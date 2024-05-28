<script setup>
import CountUp from '@/components/CountUp.vue'
import BaseButton from '@/components/BaseButton.vue'
</script>
<template>
  <h1 class="red">App</h1>
  <CountUp />
  <BaseIcon />
  <BaseButton id="base-button"/>
</template>
<style scoped>
.red {
  color: red;
}
</style>
