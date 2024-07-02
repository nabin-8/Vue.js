<script setup>
import StudentComponent from './StudentComponent.vue'
defineProps(['studentName', 'studentAge', 'studentLocation'])
</script>

<!-- <StudentComponent
  :studentName="studentName"
  :studentAge="studentAge"
  :studentLocation="studentLocation"
/> -->
<template>
  <h1>Hello From school</h1>
  <StudentComponent />
</template>
