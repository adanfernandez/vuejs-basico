<template>
  <div id="app">
    <ListadoStarWars v-on:info-detail="showInfo">
    </ListadoStarWars>

    <Detalle :detail="detail">
    </Detalle>
  </div>
</template>

<script>
import ListadoStarWars from './components/ListadoStarWars.vue'
import Detalle from "@/components/Detalle";


export default {
  name: 'App',
  data() {
    return {
      detail: null
    }
  },
  components: {
    Detalle,
    ListadoStarWars
  },
  methods: {
    showInfo(detalle) {
      this.detail = detalle;
    }
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
