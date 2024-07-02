<script setup>
import { reactive, watch } from 'vue'

const state = reactive({ username: 'alex' })

// Here we can't provide specific property of object
// - we have to provide the entire object, otherwise it's gonna give us error in the console!

/* To solve this issue
Now if we want to get the "old" 1& the "new" values separately,
- for that we'll have to pass a getter function.
- & here we have to specify the actual object/state "property".
*/
watch(
  () => state.username,
  (newValue, oldValue) => {
    // if we're using "Object" both the new & the old values will be the same
    console.log('New Value:', newValue)
    console.log('Old Value:', oldValue)
  }
)
</script>

<template>
  <h1>{{ state.username }}</h1>
  <button @click="state.username = 'Nabin'">Change Name</button>
</template>
