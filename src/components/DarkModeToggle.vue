<template>
  <div class="container mx-auto p-4">
    <button @click="toggleDarkMode" class="bg-blue-500 text-white p-2 rounded dark:bg-white dark:text-gray-800">
      切換深色模式
    </button>
  </div>
</template>


<script lang="ts">
import { ref } from 'vue';

export default {
  name: 'DarkModeToggle',
  setup() {
    const isDarkMode = ref(false);

    const toggleDarkMode = () => {
      isDarkMode.value = !isDarkMode.value;
      document.body.classList.toggle('dark', isDarkMode.value);
    };

    return {
      isDarkMode,
      toggleDarkMode,
    };
  },
};
</script>           

<style scoped>

</style>
