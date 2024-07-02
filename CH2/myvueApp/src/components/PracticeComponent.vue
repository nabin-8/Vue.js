<script setup>
import { inject } from 'vue'
const friendsList = inject('friends')
const games = inject('games')
const moreGames = inject('moreGames')
</script>

<template>
  <h4>Injecting Array</h4>
  <ul v-for="(friend, index) in friendsList" :key="index">
    <li>{{ friend }}</li>
  </ul>

  <hr />
  <h4>Injecting Object</h4>
  <ul v-for="(game, index) in games" :key="index">
    <li>{{ game }}</li>
  </ul>

  <hr />
  <h4>Array of Object</h4>
  <ul v-for="(game, index) in moreGames" :key="index">
    <li>{{ game }}</li>
  </ul>
  <hr />
  <h4>Object Destructuring</h4>
  <ul v-for="({ title, genre, platform, releseDate, developer }, index) in moreGames" :key="index">
    <li>{{ title }}</li>
    <li>{{ genre }}</li>
    <li>{{ platform }}</li>
    <li>{{ releseDate }}</li>
    <li>{{ developer }}</li>
  </ul>
</template>
