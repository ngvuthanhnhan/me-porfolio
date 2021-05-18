<template>
  <div id="app">
    <navigation-bar/>
    <introduce/>
  </div>
</template>

<script>
import Introduce from './components/Introduce.vue'
import NavigationBar from './components/NavigationBar.vue'

export default {
  name: 'App',
  components: {
    NavigationBar,
    Introduce
  }
}
</script>

<style>
* {
  background-color: #222222;
}
#app {
  font-family: 'Poppins', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
