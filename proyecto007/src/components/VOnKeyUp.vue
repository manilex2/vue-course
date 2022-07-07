<script>
    export default {
        data() {
            return {
                actividad: '',
                actividades: []
            }
        },
        methods: {
            actualizarLista: function () {
                this.actividades.push(this.actividad);
                this.actividad = '';
            }
        }
    }
</script>

<template>
    <h1>Listado de Actividades</h1>
    <ol>
        <li v-for="actividad in actividades">{{ actividad }}</li>
    </ol>
    Nueva actividad: <input type="text" v-on:keyup.enter="actualizarLista" v-model="actividad" placeholder="Enter para confirmar">
</template>