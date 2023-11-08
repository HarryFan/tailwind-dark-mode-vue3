<script setup>
import BmiCalculator from './components/BmiCalculator.vue';
import DarkModeToggle from './components/DarkModeToggle.vue';
</script>
<template>
  <main class="dark:bg-gray-800">
    <header class="bg-white dark:bg-gray-800 shadow" v-if="$route.meta.title">
      <DarkModeToggle />
      <div class="max-w-7xl mx-auto py-6 px-4 sm:px-6 lg:px-8">
        <h1 class="text-3xl font-bold leading-tight text-gray-900 dark:text-white">{{ $route.meta.title }}</h1>
      </div>
    </header>
    <router-view />
    <div class="max-w-7xl mx-auto py-6 sm:py-9 px-4 sm:px-6 lg:px-8 dark:bg-gray-800">
      <BmiCalculator />
    </div>
  </main>
</template>
