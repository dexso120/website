<template>
  <div class="home" id="main_page">
      <Intro/>
  </div>
  
</template>

<script>
// @ is an alias to /src
import Character from '@/components/game/Character.vue';
import Intro from "@/components/Intro.vue";

export default {
    name: 'HomeView',
    components: {
      Character,
      Intro
  }
}
</script>

<style scoped>
  .c.home{
    text-align: center;
    align-items: center;
    display: block;
  }
</style>