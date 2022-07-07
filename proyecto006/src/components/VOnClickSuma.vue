<script>
    export default {
        data() {
            return {
                valor1: 0,
                valor2: 0,
                suma: ""
            }
        },
        methods: {
            sumarValores: function () {
                this.suma = this.valor1 + this.valor2;
            }
        }
    }
</script>

<template>
    <p>Ingrese su numero: <input type="number" v-model="valor1"></p>
    <p>Ingrese su numero: <input type="number" v-model="valor2"></p>
    <button v-on:click="sumarValores">Sumar</button>
    <p>El resultado de la suma es igual a {{ suma }}</p>
</template>