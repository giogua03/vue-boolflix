<template>
  <div>
    <h2>FILM</h2>
    <CardComp
    v-for="objMovie in arrMovies"
    :key="objMovie.id"
      :title="objMovie.title"
      :originalTitle="objMovie.original_title"
      :language="objMovie.original_language"
      :score="objMovie.vote_average"
      :imgUrl="'https://image.tmdb.org/t/p/w342' + objMovie.poster_path"
      />
    
    <h2>SERIE TV</h2>
    <CardComp
    v-for="objTv in arrTv"
    :key="objTv.id"
      :title="objTv.name"
      :originalTitle="objTv.original_name"
      :language="objTv.original_language"
      :score="objTv.vote_average"
      :imgUrl="'https://image.tmdb.org/t/p/w342' + objTv.poster_path"
      />
  </div>
</template>

<script>
import CardComp from '@/components/CardComp.vue'
export default {
    name: 'PageMain',
    components: {
      CardComp
    },
    props:{
      arrMovies: Array,
      arrTv: Array,
    },
};
</script>

<style>

</style>



