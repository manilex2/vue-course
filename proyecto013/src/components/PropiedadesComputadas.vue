<script>
    export default {
        data() {
            return {
                nombre: '',
                apellido: ''
            }
        },
        computed: {
            nombreCompleto: function () {
                return this.nombre + ' ' + this.apellido;
            }
        }
    }
</script>

<template>
    <p>Ingrese su nombre:<input type="text" v-model="nombre"></p>
    <p>Ingrese su apellido:<input type="text" v-model="apellido"></p>
    <p>Nombre completo: {{ nombreCompleto }}</p>
</template>