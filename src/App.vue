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
    components:{
      Header,
      Nav
    }
  }
</script>

<style>

</style>
