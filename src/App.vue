<template>
  <div id="app">
<<<<<<< HEAD
    <img src="./assets/logo.png">
=======
    <Header></Header>
    <Nav></Nav>
>>>>>>> 10dcf63383ea4d20834ab0956a61006946f0f53b
    <router-view/>
  </div>
</template>

<script>
<<<<<<< HEAD
export default {
  name: 'App'
}

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  
}
=======
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

>>>>>>> 10dcf63383ea4d20834ab0956a61006946f0f53b
</style>
