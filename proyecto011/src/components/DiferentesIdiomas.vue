<script>
    export default {
        data() {
            return {
                idioma: ''
            }
        }
    }
</script>

<template>
    <p>
        <select v-model="idioma">
            <option disabled value="">Seleccione idioma</option>
            <option value="Bienvenido">Castellano</option>
            <option value="You are welcome">Ingles</option>
            <option value="seja bem vindo">Portugués</option>
            <option value="willkommen">Alemán</option>
            <option value="benvingut">Catalán</option>
            <option value="ongietorri">Euskera</option>
            <option value="bienvenue">Frances</option>
        </select>
   </p>
   <p style="font-size: 2rem">{{ idioma }}</p>
</template>