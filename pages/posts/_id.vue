<template>
  <div class="container">

      <h1 class='title'>{{ data.title.rendered }}</h1>
      <img :src="data._embedded['wp:featuredmedia'][0].source_url" />
      <div class='content' v-html="data.content.rendered"></div>
    
 
  
    
    
  </div>


</template>
<style scoped>
  .title {
    font-size: 30px;
    font-weight: 800;
    margin-bottom: 20px;
  }
  .content {
    padding:0 20px;
  }

</style>
<script>
  import axios from 'axios';
export default {
  head(){
    return {
        title:this.data.title.rendered
      }
    },
  
  async asyncData({params}){
    const id = params.id;
        let  data = [];
      const x =  await axios.get('https://chouftv.ma/wp-json/wp/v2/posts/'+id+'?_embed');

        data = x.data;
        
  return { data }
  }
}
  
</script>