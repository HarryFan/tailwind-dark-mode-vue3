<template>
  <div class="container mx-auto p-4">
    <button @click="toggleDarkMode" class="bg-blue-500 text-white p-2 rounded">
      切換深色模式
    </button>
  </div>
</template>

<script>
export default {
  name: 'DarkModeToggle',
  methods: {
    toggleDarkMode() {
      // Toggle the 'dark' class on the body element
      document.body.classList.toggle('dark');
    },
  },
};
</script>

<style scoped>
/* Scoped styles for your DarkModeToggle component */
</style>
