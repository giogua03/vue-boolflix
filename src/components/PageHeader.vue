<template>
  <div class="nav-bar">
    <form @submit.prevent="$emit('queryChange', queryString )">
      <div class="title">
        <h1>BOOLFLIX</h1>
    </div>
    <div class="serch-bar">
      <label for="query">
        <input type="text" id="query" class="yy" v-model="queryString">
      </label>
        
        <button>CERCA</button>
    </div>
    </form>
    
  </div>
</template>

<script>


export default {
 name:'PageHeader',
 data() {
  return{
    queryString:'',
  }
 }
}
</script>

<style>
  
  .nav-bar{
    height: 70px;
    background-color: blueviolet;
    color: orange;
    
  }
  form{
    display: flex;
    justify-content: space-between;
  }
  .serch-bar{
    display: flex;
    justify-content: flex-end;
    margin: 1rem;
  }
  .title{
    margin: 1rem;
    
  }
  .yy{
    padding: 0.7rem;
  }
</style>