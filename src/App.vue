<template>
  <div id="app">
    <PageHeader :results-for="searchString"/>
    <PageMain @search="search"/>
  </div>
</template>

<script>
import PageHeader from '@/components/PageHeader.vue';
import PageMain from '@/components/PageMain.vue';

export default {
  components: {
    PageHeader,
    PageMain, 
  },
  data() {
    return {
      searchString: '',
    };
  },
  methods: {
    search(data) {
      this.searchString = data;
    },
  },
};

</script>

<style lang="scss">

</style>
