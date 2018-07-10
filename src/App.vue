<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
      <app-car></app-car>
  </div>
  
</template>

<script>
import Car from './components/Car.vue'


export default {
  name: 'app',
  components: {
    Car
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
