<script setup>
import { ref } from 'vue'

const friends = ref(['Nabin', 'Jordan', 'Alex', 'Maroon 5'])
</script>

<template>
 <h3 v-for="(friend, index) in friends" :key="index">
   {{friend}}
 </h3>
</template>
