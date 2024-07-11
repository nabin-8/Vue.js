<script setup>
import { ref, computed } from 'vue'
import TodoList from './components/01TodoList/TodoList.vue'
// import Home from './App.vue'
import RandomQuoteGenerator from '@/components/02RandomQuoteGenerator/RandomQuoteGenerator.vue'
import CalculatorApp from '@/components/03Calculator/CalculatorApp.vue'
import AccordionsApp from '@/components/04Accordions/AccordionsApp.vue'
import FormValidation from '@/components/05FormValidation/FormValidation.vue'
import ProgressSteps from '@/components/06ProgressSteps/ProgressSteps.vue'
import PasswordGenerator from '@/components/07PasswordGenerator/PasswordGenerator.vue'
import DadJokes from '@/components/08DadJokes/DadJokes.vue'
import GithubUsersSearch from '@/components/09GithubUsersSearch/GithubUsersSearch.vue'
import WikiClone from '@/components/10WikiClone/WikiClone.vue'

const routes = {
  // '/Home': Home,
  '/TodoList': TodoList,
  '/RandomQuoteGenerator': RandomQuoteGenerator,
  '/CalculatorApp': CalculatorApp,
  '/AccordionsApp': AccordionsApp,
  '/FormValidation': FormValidation,
  '/ProgressSteps': ProgressSteps,
  '/PasswordGenerator': PasswordGenerator,
  '/DadJokes': DadJokes,
  '/GithubUsersSearch': GithubUsersSearch,
  '/WikiClone': WikiClone
}

// Random Quote Generator
// Calculator
// Accordions
// Form Validation
// Progress Steps
// Password Generator
// Dad Jokes
// Github Users Search
// Wiki Clone

const currentPath = ref(window.location.hash)

window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash
})

const currentView = computed(() => {
  return routes[currentPath.value.slice(1) || '/']
})
</script>

<template>
  <div class="list-container">
    <!-- <a href="#/">Home</a> -->
    <a href="#/TodoList">Todo List</a>
    <a href="#/RandomQuoteGenerator">Random Quote Generator</a>
    <a href="#/CalculatorApp">Calculator</a>
    <a href="#/AccordionsApp">Accordions</a>
    <a href="#/FormValidation">Form Validation</a>
    <a href="#/ProgressSteps">Progress Steps</a>
    <a href="#/PasswordGenerator">Password Generator</a>
    <a href="#/DadJokes">Dad Jokes</a>
    <a href="#/GithubUsersSearch">Github Users Search</a>
    <a href="#/WikiClone">Wiki Clone</a>
  </div>
  <component :is="currentView" />
  <div v-if="!currentView">
    <h1 id="vue-title"><a href="https://vuejs.org/">Vue.js</a> 10 Projects</h1>
    <ol class="home-page-div">
      <li><b>Todo List</b></li>
      <li><b>Random Quote Generator</b></li>
      <li><b>Calculator</b></li>
      <li><b>Accordions</b></li>
      <li><b>Form Validation</b></li>
      <li><b>Progress Steps</b></li>
      <li><b>Password Generator</b></li>
      <li><b>Dad Jokes</b></li>
      <li><b>Githuli Users Search</b></li>
      <li><b>Wiki Clone</b></li>
    </ol>
  </div>
</template>

<style>
#vue-title {
  text-align: center;
  margin-top: 44px;
}

#vue-title a {
  color: #334155;
}
.list-container {
  display: flex;
  gap: 20px;
  margin: 1% 5%;
}

.list-container a {
  padding: 12px;
  background-color: #334155;
  color: white;
  border-radius: 5px;
  text-decoration: none;
  /* box-shadow:
    rgba(0, 0, 0, 0.16) 0px 10px 36px 0px,
    rgba(0, 0, 0, 0.06) 0px 0px 0px 1px; */
}

.list-container a:hover {
  cursor: pointer;
  background-color: #0f172a;
}

.home-page-div {
  display: grid;
  align-items: center;
  justify-content: center;
}
@media screen and (max-width: 768px) {
  .list-container {
    display: grid;
    gap: 5px;
    margin: 1%;
  }
  .list-container a {
    padding: 8px;
    font-size: 12px;
  }
}
</style>
