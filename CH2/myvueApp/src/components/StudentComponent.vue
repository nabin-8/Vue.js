<script setup>
// defineProps(['studentName', 'studentAge', 'studentLocation'])

import { inject } from 'vue'
const studentName = inject('studentName')
const studentAge = inject('studentAge')
const studentLocation = inject('studentLocation')
</script>

<template>
  <h1>From Student {{ studentName }}</h1>
  <h1>From Student {{ studentAge }}</h1>
  <h1>From Student {{ studentLocation }}</h1>
</template>
