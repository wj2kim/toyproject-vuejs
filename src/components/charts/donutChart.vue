<template>
    <div>
        <div>
            <h3>도넛 차트 샘플</h3>
        </div>  
        <div id="chart">
            <apexcharts type="donut" height="200" :options="chartOptions" :series="series"></apexcharts>
        </div>
    </div>
</template>

<script>
import VueApexCharts from 'vue-apexcharts'

export default {
    name: 'donutChart',
    components: {
        apexcharts: VueApexCharts,
  },
    data: function() {
        return {
        series: [44, 55, 41, 17, 15],
          chartOptions: {
            chart: {
              type: 'donut',
            },
            responsive: [{
              breakpoint: 480,
              options: {
                chart: {
                  width: 200
                },
                legend: {
                  position: 'bottom'
                }
              }
            }]
          },
        }
    }
}
</script>