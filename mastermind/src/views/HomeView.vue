<script setup lang="ts">
import Message from '@/components/Message.vue'
import {
  Listbox,
  ListboxLabel,
  ListboxButton,
  ListboxOptions,
  ListboxOption,
} from '@headlessui/vue'
import { IconCheck } from '@tabler/icons-vue'
import { ref } from 'vue'
// Number to color map
const colorMap: Record<number, string> = {
  0: 'black',
  1: 'white',
  2: 'red-500',
  3: 'green-500',
  4: 'blue-500',
  5: 'yellow-500',
}

const randomValues = ref<number[] | null>(null)

const generateValues = () => {
  randomValues.value = Array.from({ length: 4 }, () => Math.floor(Math.random() * 6))
  console.log('Generated random values:', randomValues.value.map((v) => colorMap[v]).join(', '))
  // Reset the selected values for the new round
  selectedValues.value = [[null, null, null, null]]
  round.value = 0
  message.value = null
  showMessage.value = false
  title.value = null
  type.value = 'info'
}

const selectedValues = ref<(number | null)[][]>([[null, null, null, null]])
const round = ref(0)

const message = ref<string | null>(null)
const showMessage = ref(false)
const title = ref<string | null>(null)
const type = ref<'info' | 'success' | 'error'>('info')

const submitGuess = () => {
  // If there are no more rounds, return. if the guesses were all perfect, alert the user.
  if (round.value >= 9 && selectedValues.value[round.value] !== randomValues.value) {
    message.value = 'You have no more attempts left!'
    showMessage.value = true
    title.value = 'Game Over'
    type.value = 'error'
    return
  }
  if (JSON.stringify(selectedValues.value[round.value]) === JSON.stringify(randomValues.value)) {
    message.value = 'Congratulations! You guessed the combination!'
    showMessage.value = true
    title.value = 'Success'
    type.value = 'success'
    return
  }

  // If the guess is not correct, increment the round and add a new empty guess
  title.value = 'Incorrect Guess'
  type.value = 'error'
  // Calculate feedback: perfect (right color, right place), correct (right color, wrong place), wrong
  let perfect = selectedValues.value[round.value].filter(
    (value, index) => value === randomValues.value[index],
  ).length
  let correct =
    selectedValues.value[round.value].filter(
      (value) => value !== null && randomValues.value.includes(value),
    ).length - perfect

  const wrong = 4 - perfect - correct

  message.value = `Round ${round.value} started. Perfect: ${perfect}, Correct: ${correct}, Wrong: ${wrong}. You have ${10 - round.value} attempts left.`
  showMessage.value = true
  round.value++
  // Add a new empty guess for the next round
  selectedValues.value.push([null, null, null, null])
}
</script>

<template>
  <main class="flex flex-col md:flex-row items-center justify-center p-4 gap-4 w-full h-screen">
    <div
      v-if="!randomValues"
      class="flex flex-col items-start justify-center gap-2 p-4 bg-gray-100 rounded-lg shadow-md max-w-md mx-auto"
    >
      <h1>Mastermind Game</h1>
      <p>Click the button to generate a random combination of colors.</p>
      <button
        @click="generateValues"
        class="bg-green-200 rounded-md px-4 py-2 shadow-md cursor-pointer hover:shadow-lg hover:scale-105 transition-all duration-200"
      >
        Generate
      </button>
      <p>Try to guess the combination in the game!</p>
      <!-- temp cheat -->
      <div v-if="randomValues" class="text-sm text-gray-500">
        <p>Random Values: {{ randomValues.map((v) => colorMap[v]).join(', ') }}</p>
        <p>
          Selected guesses:
          {{ selectedValues[round].map((v) => (v ? colorMap[v] : null)).join(', ') }}
        </p>
      </div>
    </div>
    <!-- Game -->
    <div
      v-if="randomValues"
      class="flex flex-col items-center justify-center gap-2 p-4 bg-gray-100 rounded-lg shadow-md max-w-md mx-auto"
    >
      <h2 class="text-lg font-semibold">Round {{ round + 1 }}</h2>
      <p class="text-sm text-gray-500">You have {{ 10 - round }} attempts left.</p>
      <div
        v-for="(selectedValue, index) in selectedValues"
        class="flex items-end justify-start gap-2 p-4 w-full"
      >
        <Listbox
          as="div"
          v-for="(value, index) in selectedValue"
          :key="index"
          v-model="selectedValue[index]"
          class="w-fit flex flex-col items-center gap-2"
        >
          <ListboxLabel class="text-lg font-semibold">#{{ index + 1 }}</ListboxLabel>
          <ListboxButton
            ><div class="w-10 h-10 border rounded-md p-2" :class="`bg-${colorMap[value]}`"></div
          ></ListboxButton>
          <ListboxOptions class="bg-white border rounded-md absolute p-1 flex flex-col gap-1">
            <ListboxOption
              v-for="(color, index) in Object.keys(colorMap)"
              :key="index"
              :value="Number(color)"
              class="p-2 cursor-pointer w-10 h-10 rounded-md shadow-md"
              :class="`bg-${colorMap[color]}`"
            >
            </ListboxOption>
          </ListboxOptions>
        </Listbox>
        <button
          v-if="randomValues && index === round"
          @click="submitGuess"
          :disabled="selectedValues[round].includes(null)"
          class="bg-amber-600 disabled:bg-amber-200 disabled:shadow-none disabled:hover:shadow-none disabled:hover:scale-100 text-white rounded-lg p-2 shadow-md cursor-pointer hover:shadow-lg hover:scale-105 transition-all duration-200"
        >
          <IconCheck class="w-6 h-6 inline-block" />
        </button>
        <div v-if="index !== round" class="flex items-center justify-center">
          <div class="flex">
            <template v-if="selectedValue && randomValues">
              <template v-for="n in 4">
                <div
                  v-if="
                    selectedValue[n - 1] !== null && selectedValue[n - 1] === randomValues[n - 1]
                  "
                  :key="'green-' + n"
                  class="w-4 h-4 rounded-full m-1 bg-green-500"
                ></div>
              </template>
              <template v-for="(value, i) in selectedValue">
                <div
                  v-if="value !== null && value !== randomValues[i] && randomValues.includes(value)"
                  :key="'amber-' + i"
                  class="w-4 h-4 rounded-full m-1 bg-amber-500"
                ></div>
              </template>
            </template>
          </div>
        </div>
      </div>
      <button
        @click="generateValues"
        class="bg-green-200 rounded-md px-4 py-2 shadow-md cursor-pointer hover:shadow-lg hover:scale-105 transition-all duration-200"
      >
        Regenerate
      </button>

      <div class="hidden bg-green-500"></div>
      <div class="hidden bg-green-700"></div>
      <div class="hidden bg-red-500"></div>
      <div class="hidden bg-red-700"></div>
      <div class="hidden bg-yellow-500"></div>
      <div class="hidden bg-yellow-700"></div>
      <div class="hidden bg-blue-500"></div>
      <div class="hidden bg-blue-700"></div>
      <div class="hidden bg-white"></div>
      <div class="hidden bg-black"></div>
    </div>

    <Message
      v-if="message"
      :show="showMessage"
      :message="message"
      :title="title"
      :type="type"
      @close="showMessage = false"
    />
  </main>
</template>
