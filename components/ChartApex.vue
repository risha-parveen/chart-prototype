<template>
  <div id="chart">
    <no-ssr><ApexCharts type="bar" height="500" :options="val.chartOptions" :series="val.series"></ApexCharts></no-ssr>
  </div>
</template>

<script>
const ApexCharts = ()=> import('vue-apexcharts')
export default {
  components:{
    ApexCharts
  },
  props:{
    bgcolor:{
      type:String,
      default:'#00E396'
    }
  },
  data(){
    return {
      bg:'#00E396'
    }
  },
  watch:{
    bgcolor:function(newval,oldval){
      this.bg=newval
      this.val.chartOptions.colors.pop()
      this.val.chartOptions.colors[0]=this.bg
      console.log(this.val)
    }
  },
  computed:{ 
    val(){
      let data={
        series: [{
          data: [400, 430, 448, 470, 540, 580, 690, 1100, 1200, 1380]
        }],
        chartOptions: {
          chart: {
            type: 'bar',
            height: 500,
          },
          plotOptions: {
            bar: {
              borderRadius: 4,
              horizontal: false,
            }
          },
          colors:[this.bg],
          dataLabels: {
            enabled: false
          },
          xaxis: {
            categories: ['South Korea', 'Canada', 'United Kingdom', 'Netherlands', 'Italy', 'France', 'Japan',
              'United States', 'China', 'Germany'
            ],
          }
        },  
      } 
      return data 
    }      
    
    
  },
}
</script>

<style>

</style>