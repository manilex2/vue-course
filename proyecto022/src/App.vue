<script setup>
import Templates from "./components/Templates.vue";
defineProps({
  seleccionado: String
})
</script>

<template>
  <Templates v-bind:seleccionado="'sábado'"/>
</template>