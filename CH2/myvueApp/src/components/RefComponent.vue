<script setup>
import MyComponentRef from './MyComponentRef.vue'
import { ref, onMounted } from 'vue'

const myRef = ref(null)

onMounted(() => {
  console.log(myRef.value)
})
</script>

<template>
  <MyComponentRef ref="myRef" />
</template>
