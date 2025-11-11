<script setup lang="ts">
import { ref } from 'vue'

const userName = ref('')
</script>

<template>
  <p>User Name is: {{ userName }}</p>
  <input type="text" v-model="userName" />
  <button @click="userName = ''">Clear</button>
</template>
