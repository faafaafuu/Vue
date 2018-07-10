<template>
  <div>
    <app-counter></app-counter>

    <app-car></app-car>
  </div>
</template>

<script>
import Car from './components/Car.vue'
import Counter from './components/Counter.vue'

export default {
  components: {
    appCar: Car,
    appCounter: Counter
  }
}
</script>

<style>

</style>
