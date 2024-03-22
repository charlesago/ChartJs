<template>
  <div>
    <Doughnut
        id="my-chart-id2"
        :data="chartDatas"
        :options="chartOptionss" />

  </div>
</template>

<script lang="ts">
import { Doughnut } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js'
ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale)

export default {
  name: 'DoughnutChart',
  components: { Doughnut },
  data() {
    return {
      chartDatas: {
        labels: ['Online', 'On the Spot', 'Other', 'Telephone'],
        datasets: [ {
          backgroundColor: ['#4186b8', '#51ace4', '#00D8FF', '#2a16dd'],
          data: [50, 20, 20, 10]
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
.Barre{
  margin-top: -300px;
  margin-right:510px;
}
</style>