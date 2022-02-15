<template>
  <div class="car">
    <h2>Name: {{ carName}}</h2>
    <p>Year: {{ carYear }}</p>
  </div>
</template>

<script>
export default {
  props: ['carName', 'carYear']
}
</script>

<style scoped>
  .car {
    border: 1px solid black
  }
  .car h2 {
    margin-bottom: 5px;
  }
</style>
