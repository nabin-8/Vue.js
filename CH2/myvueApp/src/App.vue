<script setup>
// import SchoolComponent from './components/SchoolComponent.vue'
// import StudentComponent from './components/StudentComponent.vue'
// import PracticeComponent from './components/PracticeComponent.vue'
// import LifeCycleComponent from './components/LifeCycleComponent.vue'
// import BasicCompWatcher from './components/BasicCompWatcher.vue'
// import ReactiveObject from './components/ReactiveObject.vue'
// import MultipleSources from './components/MultipleSources.vue'
// import BasicRef from './components/BasicRef.vue'
// import FunctionRef from './components/FunctionRef.vue'
import RefComponent from './components/RefComponent.vue'

// import { provide } from 'vue'

// provide('studentName', 'Alex')
// provide('studentAge', 20)
// provide('studentLocation', ['Earth', 'IDK'])

// const studentName = 'alex'
// const studentAge = 22
// const studentLocation = ['Earth', 'IDK']

import { provide } from 'vue'
// Provide Array
provide('friends', ['Alex', 'Jordan', 'Nabin', 'Huxn', 'John'])

// providing Object
provide('games', {
  id: 1,
  title: 'Epic Adventure Games',
  genre: ['Action', 'Adventure'],
  platform: ['PC', 'PlayStation', 'Xbox'],
  releseDate: '2023-03-15',
  developer: {
    name: 'Awshome Game Studios',
    Location: 'San Francisco, CA',
    teamSize: 50
  }
})

// Provide Array of Object
provide('moreGames', [
  {
    title: 'Space Explorer',
    genre: 'Sci-Fi',
    platform: 'PC',
    releaseDate: '2023-05-20'
  },
  {
    title: 'Fantasy Quest',
    genre: 'Fantasy',
    platform: 'PlayStation',
    releaseDate: '2023-07-10'
  },
  {
    title: 'Inception',
    director: 'Christopher Nolan',
    genre: 'Sci-Fi',
    releaseDate: '2010-07-16'
  },
  {
    title: 'The Shawshank Redemption',
    director: 'Frank Darabont',
    genre: 'Drama',
    releaseDate: '1994-09-23'
  }
])

// component life cycle
// import { ref } from 'vue'
// const showHide = ref(false)
</script>

<!-- <SchoolComponent
  :studentName="studentName"
  :studentAge="studentAge"
  :studentLocation="studentLocation"
  <SchoolComponent /> -->
<!-- <StudentComponent /> -->

<!-- <PracticeComponent /> -->

<!-- <LifeCycleComponent v-if="showHide" />
<button @click="showHide = !showHide">Show/Hide</button> -->

<!-- <BasicCompWatcher /> -->

<!-- <ReactiveObject /> -->

<!-- <MultipleSources /> -->
<!-- <BasicRef /> -->

<!-- <FunctionRef /> -->

<template>
  <RefComponent />
</template>
