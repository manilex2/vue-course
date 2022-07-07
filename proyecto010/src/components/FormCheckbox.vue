<script>
  export default {
    data() {
      return {
        terminos: false
      }
    }
  }
</script>

<template>
  <p><input type="checkbox" v-model="terminos">Acepto los terminos y condiciones</p>
  <button v-if="terminos">Confirmar</button>
</template>