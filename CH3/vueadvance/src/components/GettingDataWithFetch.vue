<script setup>
import { ref } from 'vue'
const data=ref(null)

const fetchData=()=>{
//   Make Make a Get using fetch
  fetch('https://jsonplaceholder.typicode.com/posts').then((response)=>{
  //   check if the response status  is pk (200-299 range)

    if(!response.ok){
      throw  new Error(`HTTP Error! Status: ${response.status}`)
    }

  //   parse the JSON response
    return response.json()
  }).then((responseData)=>{
    data.value=responseData
  }).catch((error)=>{
    console.error(`Error Fetching  data: ${error}`)
  })
}
</script>

<template>
<div>
  <h1>((Using Fetch))</h1>
  <button @click="fetchData">Fetch Data</button>

  <div>
    <h2>Data from API:</h2>
    <pre>{{data}}</pre>
  </div>
</div>
</template>
