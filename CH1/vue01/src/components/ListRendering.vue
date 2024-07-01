<script setup>
import { ref } from 'vue'

let peoples = ref(['Alex', 'Jordan', 'nabin'])

const books = ref([
  {
    id: 1,
    title: 'To Kill a Mockingbird',
    author: 'Harper Lee',
    genre: 'Fiction',
    publicationYear: 1960
  },
  {
    id: 2,
    title: '1984',
    author: 'George Orwell',
    genre: 'Dystopian',
    publicationYear: 1949
  },
  {
    id: 3,
    title: 'The Great Gatsby',
    author: 'F. Scott Fitzgerald',
    genre: 'Classic',
    publicationYear: 1925
  },
  {
    id: 4,
    title: 'The Catcher in the Rye',
    author: 'J.D. Salinger',
    genre: 'Coming-of-age',
    publicationYear: 1951
  },
  {
    id: 5,
    title: "Harry Potter and the Sorcerer's Stone",
    author: 'J.K. Rowling',
    genre: 'Fantasy',
    publicationYear: 1997
  }
])

const movies = ref([
  [
    'The Shawshank Redemption',
    'The Godfather',
    'The Dark Knight',
    "Schindler's List",
    'The Green Mile'
  ],
  ['Pulp Fiction', 'Fight Club', 'Forrest Gump', 'The Silence of the Lambs', 'The Usual Suspects'],
  [
    'Inception',
    'The Matrix',
    'Interstellar',
    'Blade Runner',
    'Eternal Sunshine of the Spotless Mind'
  ],
  ['The Lord of the Rings', 'Star Wars', 'Harry Potter', 'The Hobbit', 'Jurassic Park'],
  ['Titanic', 'Avatar', 'The Terminator', 'The Sixth Sense', 'Gladiator']
])

const complexGameObj = ref({
  id: 1,
  title: 'Epic Adventure Game',
  genre: ['Action', 'Adventure', 'RPG'],
  platform: ['PC', 'PlayStation', 'Xbox', 'Nintendo Switch'],
  releaseDate: '2022-03-15',
  developer: {
    name: 'Awesome Game Studios',
    location: 'San Francisco, CA',
    teamSize: 50
  },
  ratings: {
    metacritic: 90,
    user: 4.8
  },
  features: {
    singlePlayer: true,
    multiplayer: true,
    onlineCoop: true,
    splitScreen: false
  },
  systemRequirements: {
    minimum: {
      os: 'Windows 10',
      processor: 'Intel Core i5',
      memory: '8 GB RAM',
      graphics: 'NVIDIA GTX 970',
      storage: '50 GB available space'
    },
    recommended: {
      os: 'Windows 11',
      processor: 'Intel Core i7',
      memory: '16 GB RAM',
      graphics: 'NVIDIA RTX 3080',
      storage: '100 GB available space'
    }
  },
  storyline: 'Embark on a thrilling adventure to save the world from impending doom!',
  characters: ['Hero', 'Sidekick', 'Villain', 'NPCs'],
  achievements: [
    { id: 1, name: 'Master Explorer', description: 'Explore every corner of the game world' },
    { id: 2, name: 'Legendary Warrior', description: 'Complete the game on the hardest difficulty' }
  ]
})
</script>

<template>
  <h1 v-for="(persion, index) in peoples" :key="index">{{ persion }}</h1>
  <hr />
  <div>
    <ul v-for="{ id, title, author, genre, publicationYear } in books" :key="id">
      <li>
        Title: <b>{{ title }}</b>
      </li>
      <li>
        Author: <b>{{ author }}</b>
      </li>
      <li>
        Genre: <b>{{ genre }}</b>
      </li>
      <li>
        Publication Year: <b>{{ publicationYear }}</b>
      </li>
    </ul>
  </div>
  <hr />
  <!-- <ul v-for="(game, index) in complexGameObj" :key="index"> -->
  <!-- Getting all object -->
  <!-- <li>{{ game }}</li> -->
  <!-- <br /> -->
  <!-- getting single value from object -->
  <!-- <li v-for="(property, i) in game" :key="i">
      {{ property }} -->
  <!-- </li> -->
  <!-- </ul> -->

  <ul v-for="number in 10" :key="number">
    <li>{{ number }}</li>
  </ul>
</template>
