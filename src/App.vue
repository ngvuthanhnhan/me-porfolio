<template>
  <div id="app">
    <navigation-bar/>
    <introduce/>
    <projects-container/>
    <my-footer/>
  </div>
</template>

<script>
import Introduce from './components/Introduce.vue'
import MyFooter from './components/MyFooter.vue'
import NavigationBar from './components/NavigationBar.vue'
import ProjectsContainer from './components/ProjectsContainer.vue'

export default {
  name: 'App',
  components: {
    NavigationBar,
    Introduce,
    ProjectsContainer,
    MyFooter,
  }
}
</script>

<style>
* {
  max-width: 1140px;
  margin: auto;
}
body {
  background-color: #222222 !important;
}
#app {
  font-family: 'Poppins', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #FFFFFE;
  cursor: default;
  padding-left: 7.75rem;
	padding-right: 7.75rem;
}
</style>
