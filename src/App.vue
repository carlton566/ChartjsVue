<template>
<div id="app">
    <PlanetChart/>
    <Dropdown/>
  </div>
</template>

<script>
import PlanetChart from './components/PlanetChart.vue'
import Dropdown from './components/HelloWorld.vue'



export default {
  name: 'App',
  components: {
    PlanetChart,
    Dropdown
    
  }
}
</script>


