<script setup>
const myRefFunc = (el) => {
  console.log(el)
  el.textContent = 'Text Changed'
  el.style.color = 'crimson'
}
</script>

<template>
  <h1 :ref="myRefFunc">This is a initial value</h1>
</template>
