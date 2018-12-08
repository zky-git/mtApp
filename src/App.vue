<template>
  <div id="app">
    <Header :poiInfo='poiInfo'></Header>
    <Nav :commentNum="commentNum"></Nav>
    <keep-alive><router-view/></keep-alive>
    
  </div>
</template>

<script>
  import Header  from './components/header/Header'
  import Nav  from './components/nav/Nav'
  export default {
    name: 'App',
    data(){
      return{
        poiInfo:'',
        commentNum:0
      }
    },
    components:{
      Header,
      Nav
    },
    created(){
      this.$http.get('/api/goods').then((res) => {
        if(res.data.code==0){
          this.poiInfo = res.data.data.poi_info;
        }
      }).catch((err) => {
        console.log(err)
      });
      this.$http.get('/api/ratings').then((res) => {
       
        if(res.data.code==0){
          this.commentNum= res.data.data.comment_num;
        }
      }).catch((err) => {
        
      });
    }
  }
</script>

<style>

</style>
