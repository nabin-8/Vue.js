<script setup>
import { reactive } from 'vue'
const formData = reactive({ username: '', email: '', password: '' })
const myForm = () => {
  alert(`Username: ${formData.username} Email: ${formData.email} Password: ${formData.password}`)
}
</script>

<template>
  <form action="" @submit.prevent="myForm">
    <input type="text" v-model="formData.username" placeholder="Enter your name" />
    <input type="email" v-model="formData.email" placeholder="Enter your email" />
    <input type="password" v-model="formData.password" placeholder="Enter your password" />
    <button type="submit">Submit</button>
  </form>

  <h1>username: {{ formData.username }}</h1>
  <h1>email: {{ formData.email }}</h1>
  <h1>password: {{ formData.password }}</h1>
</template>
