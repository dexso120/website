<template>
    <div class="bar" :style="{width: width}">
        
          <div class="progress" :style="{background: color, width: percent+'%'}"></div>
        
      </div>
</template>

<script>
    export default {
      name: 'Progress-bar',
      props: ['width','color', 'percent', 'padding']
  }
</script>

<style>
    .bar{
        background:#dfdfdf;
        overflow: hidden;
        padding: 3px;
        display: inline-block;
        box-sizing: border-box;
        border-radius: 25px;
    }

    .progress{
        float:left;
        padding-right: 5px;
        padding: 5px;
        box-sizing: border-box;
        border-radius: 25px;
    }

    .percent{
        float: right;
        font-weight: 600;
        height: 30px;
        line-height: 30px;
    }
</style>