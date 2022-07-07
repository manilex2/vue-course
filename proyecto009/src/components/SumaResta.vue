<script>
    export default {
        data() {
            return {
                valor1: '',
                valor2: '',
                operacion: 'suma',
                resultado: ''
            }
        },
        methods: {
            operar: function () {
                if (this.operacion === 'suma') {
                    this.resultado = parseInt(this.valor1) + parseInt(this.valor2);
                }
                if (this.operacion === 'resta') {
                    this.resultado = parseInt(this.valor1) - parseInt(this.valor2);
                }
            }
        }
    }
</script>

<template>
    <p>Ingrese primer valor: <input type="number" v-model="valor1"/></p>
    <p>Ingrese segundo valor: <input type="number" v-model="valor2"/></p>
    <p><input type="radio" v-model="operacion" value="suma"/> Sumar</p>
    <p><input type="radio" v-model="operacion" value="resta"/> Restar</p>
    <p><button v-on:click="operar">Operar</button></p>
    <p>El resultado es: {{ resultado }}</p>
</template>