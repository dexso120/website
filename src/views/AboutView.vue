<template>
  <div class="about">
    <div class="box">
      <Intro/>
    </div>
  </div>
</template>

<script>
import Intro from "@/components/Intro.vue";

export default {
      name: 'AboutView',
      components: {
        Intro
      }
    }
</script>
