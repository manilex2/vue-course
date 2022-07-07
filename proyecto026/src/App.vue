<script setup>
import { inject, onMounted, ref } from 'vue';
import ListadoArticulos from './components/ListadoArticulos.vue';
import Personas from './components/Personas.vue';

const axios = inject('axios');
defineProps({
  articulos: {
    type: Array,
    default: [
      {
        codigo: 1,
        descripcion: 'papas',
        precio: 12.52
      },
      {
        codigo: 2,
        descripcion: 'naranjas',
        precio: 21
      },
      {
        codigo: 3,
        descripcion: 'peras',
        precio: 18.20
      }
    ]
  }
});

const personas = ref([]);

onMounted(function() {
  axios.get('https://randomuser.me/api/?results=50')
  .then((respuesta) => {
    personas.value = respuesta.data.results;
  })
})
</script>

<template>
  <ListadoArticulos :articulos="articulos"></ListadoArticulos>
  <Personas :datos="personas"></Personas>
</template>