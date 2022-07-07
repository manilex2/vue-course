<script>
  export default {
    data() {
      return {
        nombre: '',
        edad: ''
      }
    }
  }
</script>

<template>
  <p>Ingrese su nombre: <input type="text" v-model="nombre"></p>
  <p>Ingrese su edad: <input type="number" v-model="edad"></p>
  <p>El nombre es {{ nombre }} y su edad {{ edad }}</p>
</template>