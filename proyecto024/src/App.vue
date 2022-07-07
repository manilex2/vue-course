<script setup>
  import SlotScope1 from "./components/SlotScope.vue";
  import NumeroAleatorio from "./components/NumeroAleatorio.vue";
  defineProps({
    minimo: Number,
    maximo: Number
  });
</script>

<template>
  <SlotScope1/>
  <SlotScope1 v-slot="valor">
    <h1>
      {{valor.nombre}} 
    </h1>
  </SlotScope1>
  <hr/>
  <SlotScope1 v-slot="valor">
    <p>
      Día:{{valor.nombre}} 
    </p>
  </SlotScope1>
  <hr/>
  <NumeroAleatorio :minimo="1" :maximo="100"/>
  <NumeroAleatorio :minimo="1" :maximo="100" v-slot="dato">
    <span style="background: black; color: white; font-size: 2rem">{{ dato.numero }}</span>
  </NumeroAleatorio>
</template>