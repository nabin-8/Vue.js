<script setup>
import { useCounter } from '@/shared/useCounter.js'

const counter=useCounter()
</script>

<template>
<h1>Count: {{counter.count}}
</h1>
  <button @click="counter.increment">Increment</button>
  <button @click="counter.decrement">Decrement</button>
</template>
