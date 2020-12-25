<template>
  
  <div class="container">
    <h2> Liste des framework</h2>
    <div class="columns">
      <div v-for="f in info" :key="f.id">
        <Card  :title="f.title"  :image="f.image" />
      </div>
      
    </div>
 </div>
  </div>
</template>

<script>
export default {
  head(){
    return {
        title:'الصفحة الرئيسية'
      }
    },
  data(){
    return {
      info:[
      {
        id:1,
        title:"Vuejs",
        image:'https://images.unsplash.com/photo-1488590528505-98d2b5aba04b?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MXx8ZGV2fGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=60'

      },
      {
        id:2,
        title:"Nodejs",
        image:'https://images.unsplash.com/photo-1543285198-3af15c4592ce?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mnx8bm9kZWpzfGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=60'
        
      },
      {
        id:3,
        title:"Laravel",
        image:'https://images.unsplash.com/photo-1579412690850-bd41cd0af397?ixid=MXwxMjA3fDB8MHxzZWFyY2h8NXx8ZGV2fGVufDB8fDB8&ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=60'
        
      }
    ]
    }
    
  },
  created(){
    console.log(this.info)
  }
}
</script>

<style scoped >
.container {
  display: flex;
  align-items: flex-start;
  justify-content: center;
  flex-direction: column;
  padding:0 20px;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}
h2 {
  font-size:22px;
}
.links {
  padding-top: 15px;
}
</style>
