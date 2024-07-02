<script setup>
import { ref, onMounted } from 'vue'

const myRef = ref('')
console.log(myRef.value)

onMounted(() => {
  console.log(myRef.value)
  myRef.value.focus()
  myRef.value.value = 'somthing '
})
</script>

<template>
  <div>
    <input type="text" placeholder="Enter your name" ref="myRef" />
  </div>
</template>
