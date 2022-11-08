<template>
  <div class="container">
    <div class="chart-container">
      <div class="left-container">
        
      </div>
      <div class="right-container">
        <div class="chart-js-container">
          <Chartjs/>
        </div>        
      </div>
    </div>
  </div>
</template>

<script>
import Chartjs from './Chartjs.vue'
export default {

}
</script>

<style lang="css">

  body {
    margin: 0px;
  }
  .container {
    height:100vh;
    width:100vw;
    background-color:rgb(225, 239, 225);
  }

  .chart-container {
    width:100%;
    height:100%;
    display:flex;
  }

  .left-container {
    width:50%;
    background-color:rgba(74, 132, 74, 0.49);
  }

  .right-container {
    width:50%;
    padding-left:20px;
  }

  .chart-js-container {
    position:relative;
    top:150px;
    height: 90%;
    width:90%;
  }

</style>