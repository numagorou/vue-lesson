<script setup>
import {
  ref,
  onMounted,
  onUnmounted,
  onUpdated,
  onBeforeMount,
  onBeforeUnmount,
  onBeforeUpdate,
  nextTick
} from 'vue'
const count = ref(0)

onMounted(() => {
  console.log('onMounted')
})
onBeforeMount(() => {
  console.log('onBeforeMount')
})
onUpdated(() => {
  console.log('onUpdated')
})
onBeforeUpdate(() => {
  console.log('onBeforeUpdate')
})
onUnmounted(() => {
  console.log('onUnmounted')
})
onBeforeUnmount(() => {
  console.log('onBeforeUnmount')
})
async function countUp() {
  count.value++
  await nextTick
  console.log('nextTick')
  debugger
}
</script>
<template>
  <p>count: {{ count }}</p>
  <button @click="countUp">+1</button>
</template>
