<script setup lang="ts">

import DarkModeToggle  from './components/DarkModeToggle.vue'
</script>

<template>
  <div>
   <DarkModeToggle />
<br>
   <div class="card">
      <!-- 卡片內容 -->
      我是卡片
    </div>

  </div>
  
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}


</style>
