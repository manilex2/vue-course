<script setup>
  import PropsVector from "./components/PropsVector.vue";
  import PropsAjax from "./components/PropsAjax.vue";
import { inject, ref } from "vue";

  const axios = inject('axios');
  const articulos = ref([]);
  defineProps({
    datos: {
      type: Array,
      default: [
        {
          codigo: 1, 
          descripcion: 'papas',
          precio: 12.52
        },{
          codigo: 2, 
          descripcion: 'naranjas',
          precio: 21
        },{
          codigo: 3, 
          descripcion: 'peras',
          precio: 18.20
        }
      ]
    }
  })
  const vMiData =  {
    created: function () {
      axios.get('http://scratchya.com.ar/vue/datos.php')
      .then((respuesta) => {
        articulos.value = respuesta.data;
      })
    } 
  }
</script>

<template>
  <PropsVector :datos="datos"/>
  <PropsAjax v-Mi-Data :articulos="articulos"/>
</template>