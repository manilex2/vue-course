<script>
    export default {
        data() {
            return {
                valor1: '',
                valor2: '',
                lista: ''
            }
        },
        methods: {
            rangoValores: function () {
                var cadena = '';
                for (let f = this.valor1; f <= this.valor2; f++) {
                    cadena += f + '-';
                }
                this.lista = cadena;
            }
        }
    }
</script>

<template>
    <form v-on:submit.prevent="rangoValores">
        <p>Ingrese el numero menor: <input type="number" v-model="valor1"></p>
        <p>Ingrese el numero mayor: <input type="number" v-model="valor2"></p>
        <p><input type="submit" value="Generar Lista"></p>
        <p>Lista de Valores: {{ lista }}</p>
    </form>
</template>