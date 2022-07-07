<script>
    export default {
        props: ['seleccionado'],
        data() {
            return {
                dias: ['lunes','martes','miércoles','jueves','viernes','sábado','domingo']
            }
        }
    }
</script>

<template>
  <div style="display: flex; flex-direction: row; justify-content: space-between; background: #ff0; font-size: 1.5rem">
    <div v-for="dia in dias">
      <span v-if="seleccionado == dia" style="background: #000; color: #fff">{{ dia }}</span>
      <span v-else>{{ dia }}</span>
    </div>
  </div>
</template>