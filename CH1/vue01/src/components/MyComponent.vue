<!-- <script setup>
// const myMessage = 'Yellow World'
// const myNumber = 100

// function add(x, y) {
//   return x + y
// }
</script> -->

<!-- <template>
  <h1>{{ myMessage }}</h1>
  <h1>{{ myNumber }}</h1>
  <h1>2 + 2 ={{ add(2, 2) }}</h1> -->
<!-- <p>{{const myName='alex'}}</p> -->
<!-- we cannot do like this -->
<!-- </template> -->

<script setup>
// const myChannel = 'https://www.youtube.com/watch?v=pgWZLS75Nmo'
// const imgLink = 'https://upload.wikimedia.org/wikipedia/en/a/aa/Hulk_%28circa_2019%29.png'
// const imgWidth = 400
// const imgHight = 400
// const imgAlt = 'just random pic'

// -------------
// Dynamic Bynding
const imgInfo = {
  src: 'https://upload.wikimedia.org/wikipedia/en/a/aa/Hulk_%28circa_2019%29.png',
  alt: 'just a random text',
  width: 400,
  height: 450
}
</script>

<template>
  <a v-bind:href="myChannel">Hux channel</a>
  <a :href="myChannel">Hux channel</a>
  <!-- <img :src="imgLink" :alt="imgAlt" :width="imgWidth" :height="imgHight" /> -->
  <img :="imgInfo" />
</template>
