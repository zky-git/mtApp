<template>
  <div id="app">
    <Header :poiInfo='poiInfo'></Header>
    <Nav></Nav>
    <router-view/>
  </div>
</template>

<script>
  import Header  from './components/header/Header'
  import Nav  from './components/nav/Nav'
  export default {
    name: 'App',
    data(){
      return{
        poiInfo:''
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
    }
  }
</script>

<style>

</style>
