<template>
  <div>
    <DonutChart></DonutChart>
    <StackedBar></StackedBar>
  </div>
</template>

<script>
import StackedBar from './charts/stackedChart';
import DonutChart from './charts/donutChart';

export default {
   name : 'StatisticsChart',
   components : {
     StackedBar,
     DonutChart
   },
   methods: {
   }
}
</script>

<style scoped>

</style>