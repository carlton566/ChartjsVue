<template>
<div class="ui two column centered grid">
  <div class="row">
        <div class="column">
            <canvas id="planet-chart"></canvas>
        </div>
        <div class="column">
            <canvas id="planet-chart1"></canvas>
        </div>
  </div>
  <div class="row">
        <div class="column">
            <canvas id="planet-chart2"></canvas>
        </div>
        <div class="column">
            <canvas id="planet-chart3"></canvas>
        </div>
  </div>
</div>

  
</template>

<script>

import Chart from 'chart.js'
import { planetChartData, planetChartData1, planetChartData2, planetChartData3  } from '../assets/js/planet-data.js'

export default {
  name: 'PlanetChart',
  data() {
    return {
      planetChartData: planetChartData,
      planetChartData1:planetChartData1,
      planetChartData2:planetChartData2,
      planetChartData3:planetChartData3
    }
  },
  mounted() {
    const ctx = document.getElementById('planet-chart');
    const ctx1 = document.getElementById('planet-chart1');
    const ctx2 = document.getElementById('planet-chart2');
    const ctx3 = document.getElementById('planet-chart3');
    new Chart(ctx, this.planetChartData);
    new Chart(ctx1, this.planetChartData1);
    new Chart(ctx2, this.planetChartData2);
    new Chart(ctx3, this.planetChartData3);
  }
}
</script>