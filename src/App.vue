<template>
  <div id="app">
    <navigation-bar/>
    <introduce/>
    <projects-container/>
  </div>
</template>

<script>
import Introduce from './components/Introduce.vue'
import NavigationBar from './components/NavigationBar.vue'
import ProjectsContainer from './components/ProjectsContainer.vue'

export default {
  name: 'App',
  components: {
    NavigationBar,
    Introduce,
    ProjectsContainer
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
  color: #FFFFFE;
}
</style>
