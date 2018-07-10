<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  <div>
    <h1>Parent: {{carName}}</h1>
    <app-car 
    :carName="carName"
    :carYear="carYear"
    ></app-car>
  </div>
  </div>
 
  
</template>

<script>
import Car from './components/Car.vue'

export default {
  name: 'app',
  data() {
    return {
      carName: 'Ford from parent',
      carYear: '1993 from parent',
    }
  },
  components: {
    appCar: Car
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
