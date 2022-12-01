<template>
  <div>
    <h2>FILM</h2>
    <ul v-for="objMovie in arrMovies" :key="objMovie.id">
      <li>{{objMovie.title}}</li>
      <li>{{objMovie.original_title}}</li>
      <li>{{objMovie.original_language}}</li>
      <li>{{objMovie.vote_average}}</li>  
    </ul>
    <h2>SERIE TV</h2>
    <ul v-for="objTv in arrTv" :key="objTv.id">
      <li>{{objTv.name}}</li>
      <li>{{objTv.original_name}}</li>
      <li>{{objTv.original_language}}</li>
      <li>{{objTv.vote_average}}</li>  
    </ul>
  </div>
</template>

<script>

export default {
    name: 'PageMain',
    props:{
      arrMovies: Array,
      arrTv: Array,
    },
};
</script>

<style>

</style>



