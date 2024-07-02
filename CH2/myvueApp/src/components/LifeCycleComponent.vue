<script setup>
import {
  ref,
  onBeforeMount,
  onMounted,
  onBeforeUpdate,
  onBeforeUnmount,
  onUpdated,
  onUnmounted
} from 'vue'

const message = ref('Hello, Vue')

// LifeCycke Hooks
onBeforeMount(() => {
  console.log('onBeforeMount: Component is about to be mounted')
})

onMounted(() => {
  console.log('onMounted: Component has been mounted')
})

onBeforeUpdate(() => {
  console.log('onBeforeUpdate: Component is about to update')
})

onUpdated(() => {
  console.log('onUpdated: Component has been updated')
})

onBeforeUnmount(() => {
  console.log('onBeforeUnmount: Component is about to be unmounted')
})

onUnmounted(() => {
  console.log('onUnmounted: component has been unmounted')
})

const updateMessage = () => {
  message.value = 'Updated Message'
}
</script>

<template>
  <p>{{ message }}</p>
  <button @click="updateMessage">Update Message</button>
</template>
