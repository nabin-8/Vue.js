<script setup>
// Basic Validation
// const props = defineProps({
//   fullname: String,
//   age: Number
// })

// Complex Validation
const props = defineProps({
  fullname: {
    type: String,
    required: true,
    default: 'Rahul'
  },
  age: Number
})
</script>
<template>
  <h1>{{ props.fullname }}</h1>
  <h1>{{ props.age }}</h1>
</template>
