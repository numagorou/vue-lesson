<script setup>
import { ref } from 'vue'
const vueURL = ref('https://vuejs.org')
const vueId = ref('vue-link')
</script>
<template>
  <a v-bind:id="vueId" v-bind:href="vueURL">Vue.js</a>
</template>
