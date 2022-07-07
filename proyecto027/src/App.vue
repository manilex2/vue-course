<script setup>
import { shallowRef, markRaw, defineAsyncComponent } from 'vue';

const Articulos = defineAsyncComponent(() => 
  import("./components/Articulos.vue")
);
const Proveedores = defineAsyncComponent(() => 
  import("./components/Proveedores.vue")
);

const Dado = defineAsyncComponent(() => 
  import("./components/Dado.vue")
);
const CartaPoker = defineAsyncComponent(() => 
  import("./components/CartaPoker.vue")
);

const componenteActual = shallowRef(Articulos);

const juego = shallowRef(Dado);

const changeArtProv = (comp) => {
  componenteActual.value = markRaw(comp);
};
const changeDadoCartas = (comp) => {
  juego.value = markRaw(comp);
};
</script>

<template>
  <button @click="changeArtProv(Articulos)">Ver artículos</button>
  <button @click="changeArtProv(Proveedores)">Ver proveedores</button>
  <component :is="componenteActual"></component>
  <button @click="changeDadoCartas(Dado)">Dados</button>
  <button @click="changeDadoCartas(CartaPoker)">Cartas</button>    
  <div>
    <component :is="juego"></component>
    <component :is="juego"></component>
    <component :is="juego"></component>
  </div>
</template>