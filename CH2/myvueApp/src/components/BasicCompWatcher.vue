<script setup>
import { ref, watch } from 'vue'

const message = ref('Hello Vue!')
const inputText = ref('app')

// watch for changes in inputText and update message accordingly
watch(inputText, (newVal, oldVal) => {
  // You can perform some logic here when input changes
  console.log(`NewVal: ${newVal}`)
  console.log(`OldVal: ${oldVal}`)
  message.value = `You typed: ${newVal}`
})
</script>

<template>
  <div>
    <h1>{{ message }}</h1>
    <input v-model="inputText" placeholder="Type somthing..." />
  </div>
</template>
