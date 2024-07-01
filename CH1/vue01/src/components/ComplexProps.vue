<script setup>
defineProps({
  friends: Array,
  userInfo: Object
})
</script>

<template>
  <!-- Iterating Over Friends Array  -->
  <ul v-for="(friend, index) in friends" :key="index">
    <h4>{{ friend }}</h4>
  </ul>
  <hr />
  <ul v-for="(info, index) in userInfo" :key="index">
    <h4>{{ info }}</h4>
  </ul>
</template>
