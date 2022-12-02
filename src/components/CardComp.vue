<template>
  <div>
    <ul >
      <li><img src="imgUrl" :alt="title"></li>
      <li>{{title}}</li>
      <li>{{originalTitle}}</li>
      <li><lang-flag iso="objMovie.original_language"/></li>
      <li>{{score}}</li>  
    </ul>
    
  </div>
</template>

<script>

import LangFlag from 'vue-lang-code-flags';
export default {
    name:'CardComp',
    components:{
      LangFlag
    },
    props:{
      title:String,
      originalTitle:String,
      language:String,
      score:Number,
      imgUrl:String,

    },
}
</script>

<style lang="scss" scoped>

</style>