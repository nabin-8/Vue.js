<script setup>
import { reactive } from 'vue'

let initialState = reactive({ val: { count: 0 }, user: ['Nabin', 'nbin'] })

const changeUser = () => {
  initialState.user[0] = 'Michel'
  initialState.user[1] = 'John'
}
</script>

<template>
  <h1>Current Count: {{ initialState.val.count }}</h1>
  <!-- <button @click="initialState.count++">+</button>
  <button @click="initialState.count--">-</button> -->
  <h2>Users: {{ initialState.user }}</h2>

  <button @click="initialState.val.count += 10">Add 10</button>
  <button @click="changeUser">Change User</button>
  <button>Add one more</button>
</template>
