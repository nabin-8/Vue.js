<script setup>
import { reactive, ref } from 'vue'
let count = ref(0)

let username = ref('')

let userList = ref(['Michel', 'jan', 'nabin', 'rahul'])

let userInfo = ref({ name: 'nabin', age: 20, location: ['KTM', 'Jhapa'], isMarrid: false })

let friends = reactive([ref('John'), ref('Alex'), ref('Nabin')])
</script>

<template>
  <h1>Count: {{ count }}</h1>
  <button @click="count++">+</button>
  <button @click="count--">-</button>

  <h1>Username: {{ username }}</h1>
  <button @click="username = 'Nabin'">Add User</button>

  <h1>UserList: {{ userList }}</h1>
  <button @click="userList.push('doe')">Add User</button>

  <hr />
  <h1>Name: {{ userInfo.name }}</h1>
  <h1>Age: {{ userInfo.age }}</h1>
  <h1>Location: {{ userInfo.location }}</h1>
  <h1>Marrid Status: {{ userInfo.isMarrid }}</h1>

  <button @click="userInfo.name = 'rahul'">Change Name</button>
  <button @click="userInfo.age = 40">Change Age</button>

  <hr />
  <h1>1.{{ friends[0] }}</h1>
  <h1>2.{{ friends[1] }}</h1>
  <h1>3.{{ friends[2] }}</h1>

  <button @click="friends[0] = '🤝'">Hand shake</button>
  <button @click="friends[1] = '🤝'">Hand shake</button>
  <button @click="friends[2] = '🤝'">Hand shake</button>
</template>
