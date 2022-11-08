<template>
  <div id="chart">
    <no-ssr><ApexCharts type="bar" height="350" :options="chartOptions" :series="series"></ApexCharts></no-ssr>
    
  </div>
</template>

<script>
const ApexCharts = ()=> import('vue-apexcharts')
export default {
  components:{
    ApexCharts
  },
  data(){       
    return {
      series: [{
        data: [400, 430, 448, 470, 540, 580, 690, 1100, 1200, 1380]
      }],
      chartOptions: {
        chart: {
          type: 'bar',
          height: 350
        },
        plotOptions: {
          bar: {
            borderRadius: 4,
            horizontal: true,
          }
        },
        dataLabels: {
          enabled: true
        },
        xaxis: {
          categories: ['South Korea', 'Canada', 'United Kingdom', 'Netherlands', 'Italy', 'France', 'Japan',
            'United States', 'China', 'Germany'
          ],
        }
      },  
    }
    
  },
}
</script>

<style>

</style>