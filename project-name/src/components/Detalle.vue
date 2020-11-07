<template>
  <div v-if="detail">
    <ul>
      <li>
        <strong>Name:</strong> {{ detail.name }}
      </li>
      <br>
      <li>
        <strong>Model:</strong> {{ detail.model }}
      </li>
      <br>
      <li>
        <strong>Manufacturer:</strong> {{ detail.manufacturer }}
      </li>
      <br>
      <li>
        <strong>Vehicle class:</strong> {{ detail.vehicle_class }}
      </li>
      <br>
      <li>
        <strong>Passengers:</strong> {{ detail.passengers }}
      </li>
      <br>
      <li>
        <strong>Crew:</strong> {{ detail.crew }}
      </li>
    </ul>
  </div>
  <div v-else>
    "Selecciona un vehículo que ver"
  </div>
</template>

<script>

export default {
  name: "Detalle",
  props: {
    detail: Object
  },
  data() {
    return {
    }
  },
  methods: {

  }
}
</script>


<style scoped>

  ul {
    list-style-type: none;
  }

  li {
    font-size: 200%;
    text-align: left;
  }

</style>
