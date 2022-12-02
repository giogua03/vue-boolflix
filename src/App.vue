<template>
  <div id="app">
    <PageHeader @queryChange="search"/>
    <PageMain :arr-movies='arrMovies' :arrTv="arrTv"/>
  </div>
</template>

<script>
import axios from 'axios';
import PageHeader from '@/components/PageHeader.vue';
import PageMain from '@/components/PageMain.vue';

export default {
  neme:'App',
  components: {
    PageHeader,
    PageMain, 
  },
  data() {
    return {
      baseApiUrl: 'https://api.themoviedb.org/3',
      apiKey:'c97c5a0688cf74d0bdab6d37a50d523c',
      resultLenguage:'it-IT',
      arrMovies:[],
      arrTv:[],
    };
  },
  methods: {
    search(queryString) {
      axios.get(this.baseApiUrl + '/search/movie',{
        params:{
          api_key: this.apiKey,
          query: queryString,
          lenguage: this.resultLenguage

        }
      })
      .then((responseAxios) => {
        this.arrMovies = responseAxios.data.results;
        console.log(this.arrMovies)
      });
      axios.get(this.baseApiUrl + '/search/tv',{
        params:{
          api_key: this.apiKey,
          query: queryString,
          lenguage: this.resultLenguage

        }
      })
      .then((responseAxios) => {
        this.arrTv = responseAxios.data.results;
        console.log(this.arrMovies)
      });
    },
  },
};

</script>

<style lang="scss">
  *{
    padding: 0;
    margin: 0;
    
  }
</style>
