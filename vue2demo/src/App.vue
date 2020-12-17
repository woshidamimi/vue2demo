<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <arc-chart></arc-chart>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ArcChart from './components/ArcChart.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    ArcChart
  },
  mounted() {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
