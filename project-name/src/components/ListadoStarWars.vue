<template>
  <div id="ListadoStarWars">
    <div>
    </div>
    <div class="lista-vehiculos">
      <ul>
        <li v-for="(vehicle, x) in list.results" v-bind:key="x">
          <span v-on:click="showInfo(vehicle.url)">{{ vehicle.name }}</span>
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
          this.list = resultado;
        })
  },
  methods: {
    showInfo(url) {
      fetch(url)
          .then(res => res.json())
          .then(detail => {
            this.$emit('info-detail', detail);
      })
    }
  }
}
</script>

<style scoped>
  ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: #333;
  }
  li {
    display: inline;
    float: left;
    color: aliceblue;
    margin-right: 2%;
  }
  li span:hover {
    background-color: #111;
  }
</style>