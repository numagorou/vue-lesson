<script setup>
import { ref } from 'vue'

const isShow = ref(true)
</script>
<template>
  <h1>Animation</h1>
  <div :class="{ 'opacity-80': isShow, 'opacity-20': !isShow, slide: !isShow }">Hello</div>
  <p>isShow:{{ isShow }}</p>
  <button @click="isShow = !isShow">show</button>
</template>
<style scoped>
div {
  transition: opacity 1s;
}

.opacity-80 {
  opacity: 0.8;
}
.opacity-20 {
  opacity: 0.2;
}
.slide {
  animation: slide 1s;
}
@keyframes slide {
  0% {
    transform: translateX(0);
  }
  50% {
    transform: translateX(100px);
  }
  100% {
    transform: translateX(0);
  }
}
</style>
