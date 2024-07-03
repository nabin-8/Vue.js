<script setup>
 // import RenderFriends from '@/components/RenderFriends.vue'
 import { ref, defineAsyncComponent } from 'vue'
 let showFriends=ref(false)
const RenderFriends=defineAsyncComponent(()=>import('./RenderFriends.vue'))
 const toggleFriends=()=>(showFriends.value=!showFriends.value)
</script>

<template>
  <div v-if="showFriends">
    <RenderFriends/>
  </div>

  <button @click="toggleFriends">Toggle Friends List</button>
</template>
