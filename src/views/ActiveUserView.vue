<template>
  <div>
    <Pie
        id="my-chart-id2"
        :data="chartDatas"
        :options="chartOptionss" />

  </div>
</template>

<script lang="ts">
import { Pie } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js'
ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale)

export default {
  name: 'ActiveUserChart',
  components: { Pie },
  data() {
    return {
      chartDatas: {
        labels: ['False 225k', 'True 25k'],
        datasets: [ {
          backgroundColor: ['#4186b8', '#51ace4', '#00D8FF', '#2a16dd'],
          data: [225000, 25000]
        } ]
      },
      chartOptionss: {
        responsive: true,
        maintainAspectRatio: false

      }
    }
  }
}



</script>



<style scoped>

</style>