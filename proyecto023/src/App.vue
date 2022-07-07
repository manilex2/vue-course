<script setup>
import Slot1 from "./components/Slot1.vue";
import MultipleSlot from "./components/MultipleSlot.vue";
import Buscadores from "./components/Buscadores.vue";
</script>

<template>
  <Slot1/>
  <hr/>
  <Slot1>
    <button>Alta</button> <button>Baja</button> <button>Modificacion</button>
  </Slot1>
  <hr/>
  <MultipleSlot>
    <template #titulo><h1>Título del mensaje</h1></template>
    <template #cuerpo><p>Cuerpo del mensaje</p></template>
    <template #pie><p>Pie del mensaje</p></template>
  </MultipleSlot>
  <hr/>
  <MultipleSlot/>
  <hr/>
  <Buscadores>
    <a href="https://duckduckgo.com">duckduckgo</a>        
    <a href="https://ask.fm">Ask</a>
  </Buscadores>
</template>
