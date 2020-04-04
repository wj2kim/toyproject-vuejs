<template>
  <div id="app">
    <h3>Toy_Project using Vue.js and Chart.js</h3>
    <Chart/>
  </div>
</template>

<script>
import Chart from './components/Chart.component.vue'

export default {
  name: 'App',
  components: {
    Chart
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
