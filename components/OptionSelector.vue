<template>
  <div class="selector-container">
    <div class="blue circle"
      @click="$emit('buttonClicked',blue)"
    ></div>
    <div class="red circle"
      @click="$emit('buttonClicked',red)"
    ></div>
    <div class="yellow circle"
      @click="$emit('buttonClicked',yellow)"
    ></div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      blue:'#4834e6',
      yellow:'#a00bab',
      red:'#1a790f'
    }
  }

}
</script>

<style>
  .selector-container {
    width:100%;
    height:100vh;
    display:flex;
    flex-direction: column;
    align-content: center;
    text-align: center;
    justify-content: center;
  }
  
  .circle {
    border-radius: 50%;
    width: 60px;
    height:60px;
    background-color: blue;
    margin:20px;
    text-align: center;
    align-content: center;
    justify-content: center;
    margin-left:auto;
    margin-right:auto;
    border: 1px solid #c9c9c9;
  }

  .blue {
    background-color:#4834e6
  }

  .yellow {
    background-color: #a00bab;
  }

  .red {
    background-color: #1a790f
  }
</style>