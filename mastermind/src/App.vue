<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header class="flex gap-0 items-center justify-start fixed top-0 start-0 w-full p-4 bg-white">
    <img alt="Vue logo" class="w-16 aspect-square object-cover" src="@/assets/logo.png" /> 
    <h1 class="font-semibold text-lg">Mastermind</h1>
  </header>

  <RouterView />
</template>

<style scoped>
</style>
