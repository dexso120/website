<template>
    <link href="@/style.css" rel="stylesheet"/>
    <img class="icon" src="@/assets/stats/profile_pic.jpg"/>
    <div class="box">
      <div class="level">
        <p>Level: 2</p>
        <Progress color="#36A1FF" percent="50" padding="10px" width="500px"></Progress>
        <p>Class: Cyber Security Analyst (Red Team)</p>
      </div>

      <div class="stats">
        
        <div id="chartdiv"></div>
        <div id="skills">
          Skill Tree: 
        </div>
      </div>
    </div>
</template>

<script>
import * as am4core from "@amcharts/amcharts4/core";
import * as am4charts from "@amcharts/amcharts4/charts";
import Progress from './Progress-bar.vue';
    export default {
    name: "Intro",
    components: { Progress },
    mounted(){

      // Import modules
      /* Create chart instance */
      let chart = am4core.create("chartdiv", am4charts.RadarChart);

      /* Add data */
      chart.data = [{
        "category": "Web Application",
        "value": 278,
      }, {
        "category": "Phishing",
        "value": 400,
      }, {
        "category": "Internal Testing",
        "value": 345,
      }, {
        "category": "Mobile Testing",
        "value": 0,
      }, {
        "category": "Network Testing",
        "value": 148,
      }, {
        "category": "Tool Development",
        "value": 287,
      }];

      /* Create axes */
      let categoryAxis = chart.xAxes.push(new am4charts.CategoryAxis());
      categoryAxis.dataFields.category = "category";
      //Axis.renderer.grid.template.disabled = true;

      let valueAxis = chart.yAxes.push(new am4charts.ValueAxis());
      valueAxis.renderer.gridType = "polygons";
      valueAxis.renderer.labels.template.disabled = true;

      /* Create and configure series */
      let series = chart.series.push(new am4charts.RadarSeries());
      series.dataFields.valueY = "value";
      series.dataFields.categoryX = "category";
      series.name = "Sales";
      series.strokeWidth = 3;
      series.zIndex = 2;
      series.strokeWidth = 3;
      series.fillOpacity = 0.5;
      series.stroke = am4core.color("#9EC8B9");
      series.fill = am4core.color("#1B4242a");
    }
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

  .level{
    text-align: center;
    align-items: center;
  }

  .stats{
    text-align: center;
    align-items: center;
    width: 70%;
    height: 70%;
    margin-left: auto;
    margin-right: auto;
  }

  #chartdiv {
	width		: 100%;
	height		: 500px;
	font-size	: 11px;
  margin: 50px 0 150px;
}

</style>