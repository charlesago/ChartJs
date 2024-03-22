<script setup lang="ts">

</script>

<template>
<div>
  <table>
    <tr class="titre">
      <th >Revenue</th>
      <th>Details</th>
    </tr>
    <tr>
      <td>Extra</td>
      <td>120,000,00</td>
    </tr>
    <tr>
      <td>Rooms</td>
      <td>300,000,00</td>
    </tr>
    <tr>
      <td>Food</td>
      <td>85,000,00</td>
    </tr>
    <tr>
      <td>Other</td>
      <td>40,000,00</td>
    </tr>
    <tr class="total">
      <td>Total</td>
      <td>500,000,00</td>
    </tr>
  </table>
</div>
</template>

<style scoped>
table, th, td {
  border:1px solid white;
  width: 600px;
  color: white;
}
.titre{
  table, th, td {
    border:2px solid white;
  }
}
.total{
  table, th, td {
    border:2px solid white;
  }
}
</style>