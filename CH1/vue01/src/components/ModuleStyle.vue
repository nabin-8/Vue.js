<template>
  <!-- <h1 v-bind:class="$style['m-class']">Using Module Css with $ syntax</h1> -->
  <h1 :class="myclasses.anotherclass">Using Module Css with $ syntax</h1>
</template>

<style module="myclasses">
.m-class {
  background: firebrick;
  color: white;
}

.anotherclass {
  background: seagreen;
  color: white;
}
</style>
