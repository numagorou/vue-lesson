<script setup>
import { ref, reactive } from 'vue'
// let a = 1
// let b = 2
// let c = a + b
// a = 4
// console.log(c)
const title = ref('Vue.js Course')
let price = ref(9.99)
console.log(price.value)
function increment() {
  price.value += 1
  console.log(price)
  instructor.age += 1
  instructor.bio = 'hi'
  instructor.sns.twitter = 'hello'
  instructor.email = ref('info.example.com')
}
const info = ref({
  student: 1000,
  rating: 4
})
const instructor = reactive({
  name: 'maruse',
  age: 25,
  sns: {
    twitter: '@__maruse__',
    youtube: '@maruse'
  },
  email: ref('maruse@example.com')
})
instructor.bio = 'hello'
const items = reactive([ref(1), ref(2), ref(3)])
items[0].value
console.log(instructor.email)
console.log(instructor.age)
console.log(info.value.student)
console.log(instructor)
</script>
<template>
  <h1>Title:{{ title }}</h1>
  <h2>Price: ${{ price - 1 }}</h2>
  <button @click="increment">button</button>
  <h2>Student:{{ info.student }}</h2>
  <h2>Instructor age:{{ instructor.age }}</h2>
  <h2>Instructor age:{{ instructor.bio }}</h2>
  <h2>Instructor SNS Twitter:{{ instructor.sns.twitter }}</h2>
  <h2>Instructor email:{{ instructor.email }}</h2>
</template>
