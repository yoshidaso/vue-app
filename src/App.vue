<script setup lang="ts">
import { reactive, ref } from 'vue'

const count = ref(0)
const increment = () => {
  count.value++
}
const incrementAge = () => {
  instructor.age++
}
const instructor = reactive({
  name: 'John',
  age: 30,
  email: 'john@example.com',
})
console.log(instructor)
</script>

<template>
  <button @click="increment">Count is: {{ count }}</button>
  <h2>Instructor name is: {{ instructor.name }}</h2>
  <h2>
    Instructor age is: {{ instructor.age }}
    <button @click="incrementAge">Increment</button>
  </h2>
</template>

<style scoped>
button {
  margin-top: 20px;
  margin-left: 20px;
  background-color: #42b983;
  color: black;
}
</style>
