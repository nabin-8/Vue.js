<script setup>
import { ref } from 'vue'
// let count = ref(0)

// const incrementCounter = () => count.value++
// const decrementCounter = () => count.value--

// const submitHandler = (e) => {
//   e.preventDefault()
//   alert('valid creadientals')
// }

const showMessage = (msg) => alert(msg)
</script>
<template>
  <h1>Count: {{ count }}</h1>
  <!-- <button v-on:click="count++">Increment</button> -->
  <!-- <button @:click="incrementCounter">Increment</button>
  <button @:click="decrementCounter">Decrement</button> -->

  <form @:submit="submitHandler">
    <!-- <input type="text" placeholder="Enter your name" />
    <input type="email" placeholder="Enter your email" />
    <button type="submit">Submit</button> -->

    <button @click="showMessage('This is my msg')">Show Message</button>
  </form>
</template>
