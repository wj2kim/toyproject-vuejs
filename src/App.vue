<template>
  <div id="app">
    <h3>Toy_Project using Vue.js and Chart.js</h3>
    <StatisticsChart/>
  </div>
</template>

<script>
import StatisticsChart from './components/StatisticsChart.vue'

export default {
  name: 'App',
  components: {
    StatisticsChart
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  margin-top: 30px;
}
</style>
