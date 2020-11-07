<template>
  <div id="app">
    <ListadoStarWars>
    </ListadoStarWars>
  </div>
</template>

<script>
import ListadoStarWars from './components/ListadoStarWars.vue'


export default {
  name: 'App',
  data() {
    return {
    }
  },
  components: {
    ListadoStarWars
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
