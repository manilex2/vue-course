<script>
    export default {
        data() {
            return {
                nombre: ''
            }
        },
        computed: {
            colorNombre: function () {
                if (this.nombre.includes(' ')) {
                    return '#f00';
                } else {
                    return '#000';
                }
            }
        }
    }
</script>

<template>
    <p>Ingrese un nombre sin espacios en blanco: <input type="text" v-model="nombre" v-bind:style="{'color': colorNombre}"></p>
</template>