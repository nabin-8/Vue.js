<script setup>
const props = defineProps(['firstname', 'lastname', 'myFavNumber'])
// console.log(props)
// props.myFavNumber = 10
</script>

<template>
  <h1>Props: {{ props.firstname }}</h1>
  <h1>Props: {{ props.lastname }}</h1>
  <h1>Props: {{ props.myFavNumber }}</h1>
</template>

<!-- props are immutable. we cannot change props value -->
