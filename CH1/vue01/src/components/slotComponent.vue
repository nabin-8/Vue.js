<script setup>
const props = defineProps(['name'])
console.log(props)
</script>

<template>
  <!-- Creating slot -->
  <slot></slot>
</template>
