<template>
  <div class="home">
    <Character/>
  </div>
  
</template>

<script>
// @ is an alias to /src
import Character from '@/components/game/Character.vue';

export default {
    name: 'HomeView',
    components: {
      Character,
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