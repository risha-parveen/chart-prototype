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
      red:'#f84e4e9d',
      blue:'#9286e997',
      yellow:'#b9b942b0'
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
    border: 1px solid rgb(201, 201, 201);
  }

  .blue {
    background-color:rgb(146, 134, 233)
  }

  .yellow {
    background-color: #dfdf39ea;
  }

  .red {
    background-color: rgb(248, 78, 78)
  }

  jfsigj{
    background-color: #f84e4e9d
  }
</style>