<template>
  <div>
  
    <div class="columns ">
      <div  v-for="x in data" class="column is-4" :key="x.id"> 
        <Card :title="x.title.rendered"
        :link="'/posts/'+x.id"
        :image="x._embedded['wp:featuredmedia'][0].source_url" />
      </div>
    </div>
    
  
  
  </div>
  
  
</template>
<style scoped>
  .columns {
    flex-wrap: wrap;
  }
</style>
<script>
  import axios from 'axios';
  export default {
    head(){
      return {
        title:' مقالات'
      }
      
    },
    async asyncData(){
      let data = [];
      const x = await axios.get("https://chouftv.ma/wp-json/wp/v2/posts?_embed")
        data = x.data;
      return { data }
  
    }
  }
</script>