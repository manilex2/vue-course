<script setup>
import HolaMundo from './components/HolaMundo.vue';
import PropsSelect from './components/PropsSelect.vue';
defineProps({
  idioma: {
    type: String,
    default: "castellano"
  }
})
</script>

<template>
  <HolaMundo idioma="ingles"/>
  <HolaMundo idioma="castellano"/>
  <p>
    <select v-model="idioma">
      <option>castellano</option>
      <option>ingles</option>
    </select>
  </p>
  <PropsSelect v-bind:idioma="idioma"/>
</template>