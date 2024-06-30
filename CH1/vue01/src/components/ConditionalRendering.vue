<script setup>
import { ref } from 'vue'
const isTrue = false
const isFalse = false

let isVisible = ref(true)

let isUserLoggedIn = ref(true)
let username = 'nabin'
let showDetails = ref(isUserLoggedIn)

const isActive = ref(true)
</script>
<template>
  <div>
    <p v-if="isTrue">This will show if true is true.</p>
    <p v-else-if="isFalse">This will show if false</p>
    <p v-else>Else this will show</p>
  </div>
  <hr />
  <div>
    <!-- v-show -->
    <button @click="isVisible = !isVisible">Toggle Visibility</button>
    <p v-show="isVisible">This Paragraph will be shown or hidden based on value os is vilibility</p>
  </div>
  <hr />

  <div>
    <h1 v-if="isUserLoggedIn">Welcome, {{ username }}</h1>
    <p v-else>Please log in to access this content</p>
    <div v-show="showDetails">
      <h4>Your Able to Modify</h4>
    </div>
  </div>

  <hr />
  <div v-if="isActive">
    <h1>My Blog Post</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Delectus, adipisci veritatis est
      consequatur ad voluptatum dolor animi quod. Totam iste ipsum corporis quos voluptatum sit quo
      minima quia officiis natus!
    </p>
  </div>
  <button @click="isActive = !isActive">Toggle Post</button>
</template>
