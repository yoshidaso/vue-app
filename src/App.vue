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
const vueURL = 'https://vuejs.org'
const vueId = ref('vue-url')
const vOnClickCount = ref(0)
const vOnClickIncrement = () => {
  vOnClickCount.value++
}
const eventName = 'keyup.k'
</script>

<template>
  <button @click="increment">Count is: {{ count }}</button>
  <h2>Instructor name is: {{ instructor.name }}</h2>
  <h2>
    Instructor age is: {{ instructor.age }}
    <button @click="incrementAge">Increment</button>
  </h2>
  <!-- <a :id="vueId" :href="vueURL">Vue URL</a> -->
  <!-- 省略記法 -->
  <a v-bind="{ id: vueId, href: vueURL }">Vue URL</a>

  <p>Count is: {{ vOnClickCount }}</p>
  <button @click="vOnClickCount++">V-ON-Click Increment</button>
  <button @click="vOnClickIncrement">V-ON-Click Function Increment</button>

  <div>
    <input type="text" @keyup.k="count++" />
    <input type="text" @[eventName]="count++" />
    <p>Count is: {{ count }}</p>
  </div>

  <vModel />
</template>

<style scoped>
button {
  margin-top: 20px;
  margin-left: 20px;
  background-color: #42b983;
  color: black;
}
</style>
