<template>

  <div class ="area">

    <form class="col s12">
      <div class="row">
        <!-- temperature input -->
        <div class = "input-field col-s4">
          <input id='temp' type = 'number' class='validate'/>
          <label for = 'temp'>Temperature...</label>
        </div>

        <!-- humidity input -->
        <div class = "input-field col-s4">
          <input id='hum' type = 'number' class='validate'/>
          <label for = 'hum'>Humidity...</label>
        </div>

        <!-- humidity input -->
        <div class = "input-field col-s4">
          <input id='pot' type = 'number' class='validate'/>
          <label for = 'pot'>Potentio...</label>
        </div>
      </div>
    </form>

  </div>

</template>

<script>
export default {

}
</script>

<style>
.area{
  width: 500px;
  height: 100px;
  margin: auto
}
</style>