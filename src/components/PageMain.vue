<template>
  <div>
    <ul v-for="objMovie in arrMovies" :key="objMovie.id">
      <li>
        {{objMovie.title}}
        <br>
        {{objMovie.original_title}}
        {{objMovie.original_lenguage}}
        {{objMovie.vote_everage}}
      </li>
    </ul>
  </div>
</template>

<script>

export default {
    name: 'PageMain',
    props:{
      arrMovies: Array,
    },
};
</script>

<style>

</style>



