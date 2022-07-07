<script>
  export default {
    data() {
      return {
        nombre: ''
      }
    }
  }
</script>

<template>
  Ingrese su nombre:
  <input type="text" v-model="nombre">
  <p>{{nombre}}</p>
</template>