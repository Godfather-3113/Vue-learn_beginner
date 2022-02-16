<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>Parent: {{ carName }}</h1>
    <v-car
      v-bind:carName="carName"
      v-bind:carYear="carYear"
    ></v-car>
  </div>

</template>

<script>
import Car from './components/Car'

export default {
  data () {
    return {
      carName: 'Ford',
      carYear: 2021
    }
  },
  components: {
    appCar: Car
  },
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
