<script>
    export default {
        data() {
            return {
                frase: '',
                cantidadLetrasa: 0
            }
        },
        methods: {
            contabilizarLetrasA: function () {
                var cant = 0;
                for(var f = 0; f < this.frase.length; f++) {
                    if (this.frase[f] == 'a' || this.frase[f] == 'A') {
                        cant++;
                    }
                }
                this.cantidadLetrasa = cant;
            }
        }
    }
</script>

<template>
    <p>Ingrese una frase: <input type="text" v-model="frase" v-on:keyup="contabilizarLetrasA" size="80"/></p>
    <p>Cantidad de letras 'a o 'A'':{{ cantidadLetrasa }}</p>
</template>