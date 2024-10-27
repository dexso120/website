<template>
  <link href="@/style.css" rel="stylesheet"/>

  <!-- Banner -->
  <div height="20%"></div>
  
  <!-- Navigation bar -->
  <div class="navbar">

      <!-- Logo -->
    <!--
      <div class="logo">
        <img id="logo" src="./assets/logo.png"/>
      </div>
    -->

    <div>
      <nav>
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
        <router-link to="/inventory">Inventory</router-link>
        <router-link to="/links">Links</router-link>
      </nav>
    </div>
    
  </div>

  <div id="main_page_container">

    <!-- Skill card on the left-->
    <div id="skill_card_space_container">
      <div id="skill_card_space">
        <Character/>
      </div>
    </div>

    <!-- Page content on the right -->
    <div id="page_content_container">
      <div id="page_content" class="box">
        <router-view/>
      </div>
    </div>

  </div>

  <!-- Footer -->
  <footer>&copy; Copyright 2024 Derrick So</footer>
  
</template>

<script>
  import Progress from '@/components/game/Progress-bar.vue';
  import Character from '@/components/game/Character.vue';

  export default {
      name: 'App',
      components: {
      Progress,
      Character,
  },
  
}
</script>

<style src=""></style>
