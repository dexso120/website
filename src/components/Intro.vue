<template>
    <div id="intro">
        <h1>Whoami?</h1>
        <p>I am a <b>Cyber Security Red Teamer.</b> </p>

        <h1>What do you do?</h1>
        <p>I simulate real life threat actor actions to better prepare clients before getting attacked by them.</p>

        <h2>Skill Matrix</h2>
        <div id="chartdiv"></div>
    </div>

    
</template>

<script>
    import * as am4core from "@amcharts/amcharts4/core";
    import * as am4charts from "@amcharts/amcharts4/charts";
    import Progress from '@/components/game/Progress-bar.vue';

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
        "category": "Fixing Printers",
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