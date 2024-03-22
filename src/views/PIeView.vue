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
  name: 'PieChart',
  components: { Pie },
  data() {
    return {
      chartDatas: {
        labels: ['Free Rooms', 'Ocuupied Rooms'],
        datasets: [ {
          backgroundColor: ['#4186b8', '#51ace4', '#00D8FF', '#2a16dd'],
          data: [80, 120]
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