<script setup>
import { ref, watch } from 'vue'

const username = ref('jordan')
const countter = ref(0)

watch([username, countter], (newVal, oldVal) => {
  console.log('New Value:', newVal)
  console.log('Old Value:', oldVal)
})
</script>

<template>
  <h1>{{ username }}</h1>
  <h1>{{ countter }}</h1>

  <button @click="username = 'Nabin'">Change Name</button>
  <button @click="countter++">Increment Counter</button>
</template>
