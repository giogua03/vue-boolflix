<template>
  <div></div>
</template>

<script>
import axios from 'axios';
import CardComponents from '@/components/CardComponents.vue';
import SearchBar from '@/components/SearchBar.vue';
export default {
    name: 'PageMain',
    components: {
      CardComponents,
      SearchBar,
    },
    data() {
      return {
        arrResponse: null,
        urlApi: 'https://api.themoviedb.org/search/movie/api_key=c97c5a0688cf74d0bdab6d37a50d523c&query=searchString',
        searchString: '', 
      };
    },
};
</script>

<style>

</style>



