<template>
  <div class="car">
    <h2>Name: {{ carName}} \ {{ reverseName }}</h2>
    <p>Year: {{ carYear }}</p>
    <button @click="changeName">Change name</button>
  </div>
</template>

<script>
export default {
  // props: ['carName', 'carYear'],
  // props: {
  //   carName: String,
  //   carYear: Number
  // },
  props: {
    carName: {
      type: String,
      required: true
      // default: 'Defautl name'
    },
    carYear: Number
  },
  methods: {
    changeName () {
      this.carName = 'Mazda'
      this.$emit('nameChanged', this.carName)
    }
  },
  computed: {
    reverseName () {
      return this.carName.split('').reverse().join('')
    }
  }
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
