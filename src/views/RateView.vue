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
  name: 'RateChart',
  components: { Bar },
  data() {
    return {
      chartData: {
        labels: [ 'Current', 'Last'  ],
        datasets: [ { data: [3000, 1400]    ,       backgroundColor: [ '#2a16dd'],
        } ]
      },
      chartOptions: {
        responsive: true
      }
    }
  }
}

</script>



<style scoped>

</style>