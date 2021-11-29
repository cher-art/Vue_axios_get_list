<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Api/>
  </div>
</template>

<script>
import Api from './services/servicesApi.vue'

export default {
  name: 'App',
  components: {
    Api
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
