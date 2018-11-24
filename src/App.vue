<template>
  <div id="app">
    <Header></Header>
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
      //fetch
      fetch("/api/goods")
      .then(res=>{
        console.log(res);
        // return res.json()
      })
      // .then(Response=>{
      //   console.log(Response)
      // })
    }
  }
</script>

<style>

</style>
