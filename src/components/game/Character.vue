<template>
    <link href="@/style.css" rel="stylesheet"/>
    <img class="icon" src="@/assets/stats/profile_pic.jpg"/>
    <div class="box">
    <div class="stats">
      <p>Level: 0</p>
      <Progress color="#36A1FF" percent="50" padding="10px" width="500px"></Progress>
      <p>Class: Cyber Security Analyst (Red Team)</p>
    </div>
  </div>
</template>

<script>
import Progress from './Progress-bar.vue';
    export default {
    name: "Intro",
    components: { Progress },
}
</script>


<style scoped>
  template{
    display: inline-flexbox;
    align-content: center;
    
  }
  
  .icon{
    width: 200px;
    height: auto;
    border-radius: 50%;
  }

  .stats{
    text-align: center;
    align-items: center;
  }

</style>