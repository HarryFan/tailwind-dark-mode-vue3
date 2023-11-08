<template>
  <div class="p-4 bg-gradient-to-r from-blue-500 to-teal-500 dark:from-gray-700 dark:to-gray-900 rounded-lg shadow-md">
    <div class="mb-4">
      <label class="block mb-2 text-white dark:text-gray-300" for="weight">Weight (kg)</label>
      <input class="w-full p-2 rounded border-0 shadow-inner bg-white dark:bg-gray-800 dark:border-gray-700 dark:text-white focus:outline-none" type="number" v-model="weight" id="weight">
    </div>
    <div class="mb-4">
      <label class="block mb-2 text-white dark:text-gray-300" for="height">Height (cm)</label>
      <input class="w-full p-2 rounded border-0 shadow-inner bg-white dark:bg-gray-800 dark:border-gray-700 dark:text-white focus:outline-none" type="number" v-model="height" id="height">
    </div>
    <button @click="calculateBmi" class="w-full bg-teal-400 hover:bg-teal-600 dark:bg-gray-600 dark:hover:bg-gray-500 text-white dark:text-white p-2 rounded transition">Calculate BMI</button>
    <div v-if="bmi" class="mt-4">
      <p class="text-white dark:text-gray-300 font-bold">Your BMI is: {{ bmi }}</p>
    </div>
  </div>
</template>


<script>
import { ref } from 'vue';

export default {
  name: 'BmiCalculator',
  setup() {
    const weight = ref(0);
    const height = ref(0);
    const bmi = ref(null);

    function calculateBmi() {
      if (weight.value > 0 && height.value > 0) {
        bmi.value = (weight.value / ((height.value / 100) ** 2)).toFixed(2);
      }
    }

    return {
      weight,
      height,
      bmi,
      calculateBmi
    };
  }
};
</script>

<style scoped>
/* Additional specific styles if needed */
</style>
