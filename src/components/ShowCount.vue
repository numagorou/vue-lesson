<script setup>
defineProps({
  foo: {
    type: [Number, String],
    default: 100
  }
})
</script>
<template>
  <p>count:{{ foo }}</p>
</template>
