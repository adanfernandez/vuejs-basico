<template>
  <div id="ListadoStarWars">
    <h2>Vehicles</h2>
    <div>
    </div>
    <div class="lista-vehiculos">
      <ul>
        <li v-for="(vehicle, x) in list.results" v-bind:key="x">
          {{ vehicle.name }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>

export default {
  name: "ListadoStarWars",
  data() {
    return {
      list: Array
    }
  },
  mounted() {
    fetch('https://swapi.dev/api/vehicles/')
        .then(res => res.json())
        .then(resultado => {
          console.log(resultado);
          this.list = resultado;
        })
  },
  methods: {
  }
}
</script>

<style scoped>
  ul {
    list-style: none;
  }
  #ListadoStarWars {
    width: 20%;
    text-align: left;
  }
</style>