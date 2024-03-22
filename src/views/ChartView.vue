<template>
  <div class="Barre">
    <Bar
        id="my-chart-id"
        :options="chartOptions"
        :data="chartData"
    />
  </div>
</template>

<script lang="ts">
import { Bar } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js'
ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale)

export default {
  name: 'BarChart',
  components: { Bar },
  data() {
    return {
      chartData: {
        labels: [ '1', '2', '3','4','5','6','7','8','9','10','11','12','13' ],
        datasets: [ { data: [40, 20, 12, 36,26,92,12,46,28,37,57,27,53],backgroundColor: ['#2a16dd'] } ]


      },
      chartOptions: {
        responsive: true
      }
    }
  }
}

</script>



<style scoped>
.Barre{

}
</style>