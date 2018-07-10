<template>
  <div id="app">
  <div>
    <h1>Parent: {{carName}}</h1>
    <app-counter></app-counter>
    <app-car 
    :carName="carName"
    :carYear="carYear"
    :changeFunc="changeNametoAudi"
    @nameChanged="carName = $event"
    @counterUpdated="$event"
    ></app-car>
  </div>
  </div>
 
  
</template>

<script>
import Car from './components/Car.vue'
import Counter from './components/Counter.vue'

export default {
  name: 'app',
  data() {
    return {
      carName: 'Ford',
      carYear: 1993,
    }
  },
  methods: {
    changeNametoAudi() {
      this.carName = 'Audi'
    }
  },
  components: {
    appCar: Car,
    appCounter: Counter,
  }
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
