<script setup>
  import SelectorNumerico from "./components/SelectorNumerico.vue";
  import { ref } from 'vue';

  defineProps({
    minimo: Number,
    maximo: Number
  });

  defineEmits([
    'incremento',
    'decremento'
  ]);

  const suma = ref(0);
  
  const sumar = (valor) => {
    suma.value += valor; 
  };
</script>

<template>
  <SelectorNumerico @incremento="sumar(1);" @decremento="sumar(-1)" :valor="0" :minimo="0" :maximo="20"></SelectorNumerico>
  <SelectorNumerico @incremento="sumar(1);" @decremento="sumar(-1)" :valor="0" :minimo="0" :maximo="20"></SelectorNumerico>
  <SelectorNumerico @incremento="sumar(1);" @decremento="sumar(-1)" :valor="0" :minimo="0" :maximo="20"></SelectorNumerico>
  <p>La suma es: {{suma}}</p>
</template>