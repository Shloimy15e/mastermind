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

const randomValues = ref<(number | null)[] | null>(null)

const generateValues = () => {
  randomValues.value = Array.from({ length: 4 }, () => Math.floor(Math.random() * 6))
  console.log('Generated random values:', randomValues.value.map((v) => v ? colorMap[v] : null).join(', '))
  // Reset the selected values for the new round
  selectedValues.value = [[null, null, null, null]]
  round.value = 0
  message.value = null
  showMessage.value = false
  title.value = undefined
  type.value = 'info'
}

const selectedValues = ref<(number | null)[][]>([[null, null, null, null]])
const round = ref(0)

const message = ref<string | null>(null)
const showMessage = ref(false)
const title = ref<string | undefined>(undefined)
const type = ref<'info' | 'success' | 'error'>('info')

const perfect = ref<number[]>([0])
const correct = ref<number[]>([0])

const submitGuess = () => {
  // If there are no more rounds, return. if the guesses were all perfect, alert the user.
  if (round.value >= 9 && selectedValues.value[round.value] !== randomValues?.value) {
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
  let guess = [...selectedValues.value[round.value]]
  let answerCopy = [...randomValues.value || []]
  guess.forEach((value, i) => {
    if (value !== null && answerCopy[i] !== null && value === answerCopy[i]) {
      if (!perfect.value[round.value]) {
        perfect.value[round.value] = 0
      }
      perfect.value[round.value]++
      guess[i] = null // Mark as counted
      // Remove the value from randomValues to avoid counting it again
      answerCopy[i] = null
    }
    return
  })

  // Count correct guesses (right color, wrong place)
  guess.forEach((value, i) => {
    if (value !== null && answerCopy !== null && answerCopy.includes(value)) {
      if (!correct.value[round.value]) {
        correct.value[round.value] = 0
      }
      correct.value[round.value]++
    }
  })

  const wrong = 4 - perfect.value[round.value] - correct.value[round.value]

  message.value = `Round ${round.value} started. Perfect: ${perfect.value[round.value]}, Correct: ${correct.value[round.value]}, Wrong: ${wrong}. You have ${10 - round.value} attempts left.`
  showMessage.value = true
  round.value++
  // Add a new empty guess for the next round
  selectedValues.value.push([null, null, null, null])
  console.log('Perfect:', perfect.value[round.value - 1], 'Correct:', correct.value[round.value - 1])
}
</script>

<template>
  <div class="min-h-screen bg-gradient-to-br from-slate-50 via-gray-50 to-blue-50 dark:from-slate-900 dark:via-gray-900 dark:to-slate-800 relative overflow-hidden">
    <!-- Background Elements -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute inset-0 opacity-20">
        <div class="absolute top-0 left-0 w-full h-full bg-gradient-to-r from-blue-500/8 via-purple-500/8 to-indigo-500/8"></div>
      </div>
      
      <!-- Floating Elements -->
      <div class="absolute inset-0">
        <div class="absolute top-[15%] left-[5%] w-20 h-20 bg-gradient-to-br from-blue-400/15 to-indigo-600/15 rounded-2xl opacity-40 animate-float transform rotate-12"></div>
        <div class="absolute top-[25%] right-[8%] w-16 h-16 bg-gradient-to-br from-indigo-400/15 to-purple-600/15 rounded-full opacity-30 animate-float-delay"></div>
        <div class="absolute bottom-[20%] left-[15%] w-24 h-24 bg-gradient-to-br from-purple-400/15 to-pink-600/15 rounded-xl opacity-25 animate-float"></div>
        <div class="absolute top-[60%] right-[20%] w-14 h-14 bg-gradient-to-br from-pink-400/10 to-blue-600/10 rounded-lg opacity-20 animate-float-delay"></div>
      </div>
    </div>

    <div class="relative z-10 min-h-screen grid grid-rows-[auto_1fr_auto] gap-0">
      <!-- Content Container -->
      <div class="grid place-items-center gap-16 px-6 py-12">
        
        <!-- Header Section -->
        <div class="grid place-items-center gap-8 text-center max-w-3xl">
          <div class="inline-flex items-center px-5 py-2.5 rounded-full bg-white/90 dark:bg-gray-800/90 backdrop-blur-xl border border-gray-200/60 dark:border-gray-700/60 shadow-lg">
            <div class="w-1.5 h-1.5 bg-gradient-to-r from-blue-500 to-purple-500 rounded-full animate-pulse mr-2.5"></div>
            <span class="text-xs font-medium text-gray-700 dark:text-gray-300 tracking-wide">LOGIC PUZZLE GAME</span>
          </div>
          
          <h1 class="text-4xl sm:text-5xl lg:text-6xl font-black leading-[0.9] tracking-tight">
            <span class="block bg-gradient-to-r from-gray-900 via-blue-800 to-indigo-900 dark:from-white dark:via-blue-200 dark:to-indigo-200 bg-clip-text text-transparent">
              Mastermind
            </span>
            <span class="block bg-gradient-to-r from-indigo-800 via-purple-800 to-blue-900 dark:from-indigo-200 dark:via-purple-200 dark:to-blue-200 bg-clip-text text-transparent">
              Challenge
            </span>
          </h1>
          
          <p class="text-lg sm:text-xl leading-[1.6] font-light text-gray-600 dark:text-gray-300">
            Crack the secret color combination using 
            <span class="font-semibold text-blue-600 dark:text-blue-400">deductive reasoning</span> and 
            <span class="font-semibold text-indigo-600 dark:text-indigo-400">logical thinking</span>
          </p>
        </div>

        <!-- Game Content -->
        <div class="grid place-items-center gap-12 w-full">
          <!-- Start Game Screen -->
          <div v-if="!randomValues" class="w-full max-w-md">
            <div class="bg-white/80 dark:bg-gray-800/80 backdrop-blur-xl rounded-2xl border border-gray-200/50 dark:border-gray-700/50 shadow-xl p-8">
              <div class="grid place-items-center gap-6">
                <div class="w-16 h-16 bg-gradient-to-r from-blue-500 to-indigo-500 rounded-2xl grid place-items-center">
                  <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M11.3 1.046A1 1 0 0112 2v5h4a1 1 0 01.82 1.573l-7 10A1 1 0 018 18v-5H4a1 1 0 01-.82-1.573l7-10a1 1 0 011.12-.38z" clip-rule="evenodd"/>
                  </svg>
                </div>
                
                <div class="grid gap-4 text-center">
                  <h2 class="text-2xl font-bold text-gray-900 dark:text-white">Ready to Play?</h2>
                  <p class="text-gray-600 dark:text-gray-300 leading-relaxed">
                    I'll generate a secret combination of 4 colors. Your goal is to guess the exact sequence within 10 attempts using the feedback clues.
                  </p>
                </div>
                
                <button
                  @click="generateValues"
                  class="group relative w-full px-8 py-4 bg-gradient-to-r from-blue-600 to-indigo-600 hover:from-blue-700 hover:to-indigo-700 text-white font-semibold rounded-xl transition-all duration-300 transform hover:-translate-y-1 hover:shadow-lg focus:outline-none focus:ring-4 focus:ring-blue-500/50"
                >
                  <span class="relative z-10">Generate Secret Code</span>
                  <div class="absolute inset-0 rounded-xl bg-gradient-to-r from-white/20 to-white/10 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                </button>

                <div class="grid gap-2 text-sm text-gray-500 dark:text-gray-400">
                  <p>🔴 Perfect: Right color, right position</p>
                  <p>🟡 Correct: Right color, wrong position</p>
                </div>
              </div>
            </div>
          </div>

          <!-- Game Board -->
          <div v-if="randomValues" class="w-full max-w-2xl">
            <div class="bg-white/80 dark:bg-gray-800/80 backdrop-blur-xl rounded-2xl border border-gray-200/50 dark:border-gray-700/50 shadow-xl p-8">
              <div class="grid gap-8">
                <!-- Game Header -->
                <div class="grid grid-cols-2 gap-4 place-items-center">
                  <div class="px-4 py-2 bg-blue-100 dark:bg-blue-900/30 rounded-full">
                    <span class="text-sm font-semibold text-blue-700 dark:text-blue-300">Round {{ round + 1 }}</span>
                  </div>
                  <div class="px-4 py-2 bg-indigo-100 dark:bg-indigo-900/30 rounded-full">
                    <span class="text-sm font-semibold text-indigo-700 dark:text-indigo-300">{{ 10 - round }} attempts left</span>
                  </div>
                </div>

                <!-- Guess Rows -->
                <div class="grid gap-4">
                  <div
                    v-for="(selectedValue, rowIndex) in selectedValues"
                    :key="rowIndex"
                    class="grid grid-cols-[auto_1fr_auto] gap-4 items-center p-4 rounded-xl border"
                    :class="rowIndex === round ? 'bg-blue-50/80 dark:bg-blue-900/20 border-blue-200 dark:border-blue-700' : 'bg-gray-50/50 dark:bg-gray-700/30 border-gray-200 dark:border-gray-600'"
                  >
                    <!-- Row Number -->
                    <span class="text-sm font-medium text-gray-700 dark:text-gray-300 w-8">{{ rowIndex + 1 }}.</span>
                    
                    <!-- Color Selection Grid -->
                    <div class="grid grid-cols-4 gap-3 justify-items-center">
                      <Listbox
                        as="div"
                        v-for="(value, colorIndex) in selectedValue"
                        :key="colorIndex"
                        v-model="selectedValue[colorIndex]"
                        class="relative"
                      >
                        <ListboxButton class="group">
                          <div
                            class="w-12 h-12 rounded-xl border-2 border-gray-300 dark:border-gray-600 transition-all duration-200 group-hover:scale-105 group-hover:shadow-md"
                            :class="value !== null ? `bg-${colorMap[value]}` : 'bg-gray-200 dark:bg-gray-600'"
                          ></div>
                        </ListboxButton>
                        <ListboxOptions class="absolute z-50 mt-2 bg-white dark:bg-gray-800 border border-gray-200 dark:border-gray-600 rounded-xl p-2 shadow-xl backdrop-blur-xl">
                          <div class="grid grid-cols-3 gap-2">
                            <ListboxOption
                              v-for="(color, colorKeyIndex) in Object.keys(colorMap)"
                              :key="colorKeyIndex"
                              :value="Number(color)"
                              class="w-10 h-10 rounded-lg cursor-pointer transition-all duration-200 hover:scale-110 hover:shadow-md"
                              :class="`bg-${colorMap[Number(color)]}`"
                            >
                            </ListboxOption>
                          </div>
                        </ListboxOptions>
                      </Listbox>
                    </div>

                    <!-- Submit Button or Feedback -->
                    <div class="grid place-items-center">
                      <button
                        v-if="randomValues && rowIndex === round"
                        @click="submitGuess"
                        :disabled="selectedValues[round].includes(null)"
                        class="group relative px-6 py-3 bg-gradient-to-r from-emerald-600 to-green-600 hover:from-emerald-700 hover:to-green-700 disabled:from-gray-400 disabled:to-gray-500 text-white font-semibold rounded-xl transition-all duration-300 transform hover:-translate-y-1 hover:shadow-lg disabled:transform-none disabled:shadow-none focus:outline-none focus:ring-4 focus:ring-emerald-500/50"
                      >
                        <span class="relative z-10 grid grid-cols-[auto_auto] gap-2 items-center">
                          <IconCheck class="w-5 h-5" />
                          <span>Submit</span>
                        </span>
                        <div class="absolute inset-0 rounded-xl bg-gradient-to-r from-white/20 to-white/10 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                      </button>
                      
                      <!-- Feedback Dots -->
                      <div v-if="rowIndex !== round" class="grid grid-flow-col gap-1">
                        <template v-if="selectedValue && randomValues">
                          <template v-for="n in perfect[rowIndex]" :key="'perfect-' + n">
                            <div class="w-4 h-4 rounded-full bg-emerald-500 border border-emerald-600"></div>
                          </template>
                          <template v-for="n in correct[rowIndex]" :key="'correct-' + n">
                            <div class="w-4 h-4 rounded-full bg-amber-500 border border-amber-600"></div>
                          </template>
                        </template>
                      </div>
                    </div>
                  </div>
                </div>

                <!-- Action Button -->
                <div class="grid place-items-center">
                  <button
                    @click="generateValues"
                    class="group relative px-8 py-4 bg-gradient-to-r from-indigo-600 to-purple-600 hover:from-indigo-700 hover:to-purple-700 text-white font-semibold rounded-xl transition-all duration-300 transform hover:-translate-y-1 hover:shadow-lg focus:outline-none focus:ring-4 focus:ring-indigo-500/50"
                  >
                    <span class="relative z-10">New Game</span>
                    <div class="absolute inset-0 rounded-xl bg-gradient-to-r from-white/20 to-white/10 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                  </button>
                </div>
              </div>
            </div>
          </div>

          <!-- How to Play Section -->
          <div v-if="randomValues" class="w-full max-w-4xl">
            <div class="bg-white/70 dark:bg-gray-800/70 backdrop-blur-xl rounded-xl p-6 border border-gray-200/40 dark:border-gray-700/40 shadow-md">
              <div class="grid gap-6">
                <h3 class="text-lg font-bold text-gray-900 dark:text-white text-center">How to Play</h3>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6 text-sm text-gray-600 dark:text-gray-300">
                  <div class="grid grid-cols-[auto_1fr] gap-3 items-start">
                    <div class="w-6 h-6 bg-emerald-500 rounded-full grid place-items-center">
                      <span class="text-white text-xs font-bold">1</span>
                    </div>
                    <div class="grid gap-1">
                      <h4 class="font-semibold text-gray-900 dark:text-white">Select Colors</h4>
                      <p>Click on each circle to choose from 6 available colors for your guess.</p>
                    </div>
                  </div>
                  <div class="grid grid-cols-[auto_1fr] gap-3 items-start">
                    <div class="w-6 h-6 bg-emerald-500 rounded-full grid place-items-center">
                      <span class="text-white text-xs font-bold">2</span>
                    </div>
                    <div class="grid gap-1">
                      <h4 class="font-semibold text-gray-900 dark:text-white">Submit Guess</h4>
                      <p>Once all 4 colors are selected, click Submit to see your feedback.</p>
                    </div>
                  </div>
                  <div class="grid grid-cols-[auto_1fr] gap-3 items-start">
                    <div class="w-6 h-6 bg-emerald-500 rounded-full grid place-items-center">
                      <span class="text-white text-xs font-bold">3</span>
                    </div>
                    <div class="grid gap-1">
                      <h4 class="font-semibold text-gray-900 dark:text-white">Read Feedback</h4>
                      <p>🟢 Perfect: Right color in right position. 🟡 Correct: Right color in wrong position.</p>
                    </div>
                  </div>
                  <div class="grid grid-cols-[auto_1fr] gap-3 items-start">
                    <div class="w-6 h-6 bg-emerald-500 rounded-full grid place-items-center">
                      <span class="text-white text-xs font-bold">4</span>
                    </div>
                    <div class="grid gap-1">
                      <h4 class="font-semibold text-gray-900 dark:text-white">Crack the Code</h4>
                      <p>Use feedback to deduce the secret combination within 10 attempts!</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Hidden color classes for Tailwind -->
      <div class="hidden bg-green-500 bg-green-700 bg-red-500 bg-red-700 bg-yellow-500 bg-yellow-700 bg-blue-500 bg-blue-700 bg-white bg-black"></div>
    </div>

    <Message
      v-if="message"
      :show="showMessage"
      :message="message"
      :title="title"
      :type="type"
      @close="showMessage = false"
    />
  </div>
</template>

<style scoped>
/* Animations */
@keyframes float {
  0%, 100% { transform: translateY(0px) rotate(12deg); }
  50% { transform: translateY(-6px) rotate(12deg); }
}

@keyframes float-delay {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-8px); }
}

.animate-float {
  animation: float 3.5s ease-in-out infinite;
}

.animate-float-delay {
  animation: float-delay 4.2s ease-in-out infinite;
}

/* Smooth Transitions */
* {
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
}
</style>
