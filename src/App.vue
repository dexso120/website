<template>

  <!-- Navigation bar -->
  <div class="navbar">
    <div class="health-bar">
      <p>HP: 100 <Progress color="green" percent="100" padding="5px" width="200px"></Progress></p>
      <p>MP: 100 <Progress color="blue" percent="100" padding="5px" width="200px"></Progress></p>
    </div>

    <!-- Logo -->
  <!--
    <div class="logo">
      <img id="logo" src="./assets/logo.png"/>
    </div>
  -->

  <div class="align-right">
    <nav>
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/inventory">Inventory</router-link>
      <router-link to="/links">Links</router-link>
    </nav>
  </div>
    
  </div>

  <!-- Page content -->
  <div class="content">
    <router-view/>
  </div>

  
</template>

<script>
  import Progress from '@/components/game/Progress-bar.vue';

  export default {
      name: 'App',
      components: {
      Progress,
  }
}
</script>

<style>
  html{
    height: 100%;
    width: 100%;
    background-color: #FFFFFF;
  }
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  
}

.navbar{
  height: auto;
  width: auto;
  overflow: hidden;
  box-sizing: border-box;
  align-items: center;
}

nav {
  padding: 20px;
  float: right;
  height: fit-content;
  width: 30%;
  box-sizing: border-box;
}

nav a {
  font-weight: bold;
  color: white;
  background-color: #FF8E91;
  padding: 15px;
  width: fit-content;
  box-sizing: border-box;
}

nav a.router-link-exact-active {
  background-color: #E64146;
}

.health-bar{
  float: left;
  text-align: left;
  width: 40%;
  box-sizing: border-box;
}

.align-right{
  margin-left: auto; 
margin-right: 0;
}
</style>
