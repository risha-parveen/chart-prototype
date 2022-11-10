<template>
  <Bar
    :chart-options="val.chartOptions"
    :chart-data="val.chartData"
    :chart-id="chartId"
    :dataset-id-key="datasetIdKey"
    :plugins="plugins"
    :css-classes="cssClasses"
    :styles="styles"
    :width="width"
    :height="height"
  />
</template>

<script>
import { Bar } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale)

export default {
  components: { Bar },
  props: {
    chartId: {
      type: String,
      default: 'bar-chart'
    },
    datasetIdKey: {
      type: String,
      default: 'label'
    },
    width: {
      type: Number,
      default: 400
    },
    height: {
      type: Number,
      default: 400
    },
    cssClasses: {
      default: '',
      type: String
    },
    styles: {
      type: Object,
      default: () => {}
    },
    plugins: {
      type: Object,
      default: () => {}
    },
    bgcolor:{
      type:String,
      default: ''
    }
  },
  watch:{
    bgcolor:function(newval,oldval){
      this.bg=[newval]
    }
  },
  data() {
    return {
      bg:['rgba(255, 99, 132)','rgba(0, 255, 0)','rgba(255, 99, 132)','rgba(255, 255, 128)']
    }
  },
  computed:{
    val(){
      const data = {
        chartData: {
          labels: [ 0,1,2,3,4,5,6,7,8,9,10 ],
          datasets: [ {
            data: [40, 20, 12, 70,60,14,32,35,67,19,11],
            label: 'Frequency',
            backgroundColor: this.bg,
            borderRadius:5,
            opacity:0.5,
          } ]
        },
        chartOptions: {
          responsive: true,
          plugins:{
            title: {
              display: true,
              text: 'Chart made using vue chartjs'
            },
          },
          scales: {
            y: {
              title: {
                display: true,
                text: 'Frequency'
              }
            },
            x: {
              title: {
                display: true,
                text: 'Values'
              }
            }
          }
        },
      }
      return data
    }
  }
}
</script>
