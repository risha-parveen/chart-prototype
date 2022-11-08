<template>
  <div class="container">
    <div class="chart-container">
      <div class="left-container">
        
      </div>
      <div class="right-container">
        <div class="chart-js-container">
          <ChartApex/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ChartApex from './ChartApex.vue'
export default {
  components: { ChartApex }
}
</script>

<style lang="css">

  body {
    margin: 0px;
  }
  .container {
    height:100vh;
    width:100vw;
    background-color:rgb(219, 237, 255);
  }

  .chart-container {
    width:100%;
    height:100%;
    display:flex;
  }

  .left-container {
    width:50%;
    background-color:rgba(56, 157, 252, 0.326);
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