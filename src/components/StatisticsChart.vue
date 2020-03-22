<template>

  <div class ="area">
    <form class="col s12">
      <div class="row">
        <!-- temperature input -->
        <div class = "input-field col s3">
          <input id='temp' type = 'number' class='validate'/>
          <label for = 'temp'>Temperature...</label>
        </div>

        <!-- humidity input -->
        <div class = "input-field col s3">
          <input id='hum' type = 'number' class='validate'/>
          <label for = 'hum'>Humidity...</label>
        </div>

        <!-- humidity input -->
        <div class = "input-field col s3">
          <input id='pot' type = 'number' class='validate'/>
          <label for = 'pot'>Potentio...</label>
        </div>

        <div class = "col s3">
          <div class ="row">

            <!-- get button -->
            <a class ="col s6 waves-effect waves-light btn-large teal lighten-2">
              <i class="meterial-icons">
                cloud_download
              </i>
            </a>

            <!-- post button -->
            <a class ="col s6 waves-effect waves-light btn-large pink lighten-2">
              <i class="meterial-icons">
                cloud_upload
              </i>
            </a>
          </div>
        </div>
      </div>
    </form>

    <!-- chart.js component -->
    <LineChart
      :chart-data = 'datacollection'
    >
    </LineChart>
  </div>

</template>

<script>
import LineChart from './StatisticsLine.js'

export default {
  components : {
    LineChart
  },
  data(){
    return {
      datacollection : null,
      loaded : false,
      temperature: [0,1,2,3,4,5,6,7,8,9],
      humidity: [9,8,7,6,5,4,3,2,1,0],
      potentio: [4,6,4,6,4,6,4,6,4,6],
      time: [0,1,2,3,4,5,6,7,8,9]
    }
  },
  mounted(){
    this.fillData()
  },
  methods : {
    fillData(){
      this.datacollection = {
        labels : this.time,
        datasets : [
          {
            label : 'Temp (°C)',
            backgroundColor : 'rgba(255,0,0,0.2)',
            borderColor : 'lightblue',
            pointBackgroundColor : 'red',
            borderWidth: 1,
            pointBorderColor : 'red',
            data : this.temperature
          },
          {
            label : 'Hum (%)',
            backgroundColor : 'rgba(0,0,255,0.2)',
            borderColor : 'lightblue',
            pointBackgroundColor : 'blue',
            borderWidth: 1,
            pointBorderColor : 'blue',
            data : this.humidity
          },
          {
            label : 'Potentio',
            backgroundColor : 'rgba(255,255,0,0.2)',
            borderColor : 'orange',
            pointBackgroundColor : 'orange',
            borderWidth: 1,
            pointBorderColor : 'orange',
            data : this.potentio
          }
        ]
      }
    }
  }
}
</script>

<style>
.area{
  width: 500px;
  height: 100px;
  margin: auto
}
</style>