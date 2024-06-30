<script setup>
import { ref, computed } from 'vue'

const number = ref(5)
const squaredNumber = computed(() => {
  return number.value * number.value
})

const fname = ref('Nabin')
const lname = ref('WebDev')

const fullName = computed(() => fname.value + ' ' + lname.value)

const counter = ref(0)
const squaredCounter = computed(() => counter.value ** 2)

const incrementCount = () => {
  counter.value++
}
</script>

<template>
  <h1>Original Nymber: {{ number }}</h1>
  <h1>Square Nymber: {{ squaredNumber }}</h1>
  <hr />

  <h1>Full Name: {{ fullName }}</h1>
  <hr />

  <h1>Counter: {{ counter }}</h1>
  <p>Square: {{ squaredCounter }}</p>
  <button @click="incrementCount">Increment Counter</button>
</template>
