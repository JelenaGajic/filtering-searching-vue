<template>
  <h1>Filters:</h1>

  <label for="search">Search</label>
  <input type="text" id="search" v-model="term" @keyup.enter="search(term)"/>

  <p v-for="filter in filters" :key="filter" @click="() => filterPosts(filter)">
    {{ filter }}
  </p>
</template>

<script>

const filters = [
  'All',
  'EIFS',
  'Overhead Doors'
]

export default {
  props: [
    'filterPosts',
    'search'
  ],
  data () {
    return {
      filters,
      term: ''
    };
  }
}
</script>
