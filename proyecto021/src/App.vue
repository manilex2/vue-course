<script setup>
  import MetodosModelos from "./components/MetodosModelos.vue";
import ButtonIncrementar from "./components/ButtonIncrementar.vue";
  defineProps({
    valor: Number,
    minimo: Number,
    maximo: Number
  })
</script>

<template>
  <MetodosModelos v-bind:valor="1" v-bind:minimo="0" v-bind:maximo="20"/>
  <ButtonIncrementar/>
</template>