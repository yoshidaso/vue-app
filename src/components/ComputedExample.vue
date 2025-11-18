<script setup lang="ts">
import { ref, computed } from 'vue'

const count = ref(0)
const doubleCount = computed(() => (count.value > 3 ? 'Yes' : 'No'))
</script>

<template>
  <p>Count is: {{ count }}</p>
  <p>Count is greater than 3: {{ doubleCount }}</p>
  <button @click="count++">Increment</button>
</template>
