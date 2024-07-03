<script setup>
import { ref } from 'vue'

import ComponentOne from '@/components/ComponentOne.vue'
import ComponentTwo from '@/components/ComponentTwo.vue'

const currentTab=ref('ComponentOne')

const tabs={
  ComponentOne,
  ComponentTwo
}
</script>

<template>
<h1>Main Component</h1>
  <button @click="currentTab='ComponentOne'">What is HTML?</button>
  <button @click="currentTab='ComponentTwo'">What is JS?</button>

<!--  Dynamic Component-->
  <component :is="tabs[currentTab]" />
</template>
