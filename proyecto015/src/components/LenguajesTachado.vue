<script>
    export default {
        data() {
            return {
                lenguajes: [
                    {
                        nombre: 'C',
                        tachado: false
                    },
                    {
                        nombre: 'Java',
                        tachado: false
                    },
                    {
                        nombre: 'PHP',
                        tachado: false
                    },
                    {
                        nombre: 'Python',
                        tachado: false
                    },
                    {
                        nombre: 'Ruby',
                        tachado: false
                    },
                    {
                        nombre: 'Kotlin',
                        tachado: false
                    },
                    {
                        nombre: 'C#',
                        tachado: false
                    }
                ]
            }
        },
        methods: {
            presion: function (lenguaje) {
                lenguaje.tachado = true;
            }
        }
    }
</script>

<template>
    <ul style="font-size:2rem; list-style:none">
        <li v-for="lenguaje in lenguajes" v-on:click="presion(lenguaje)" v-bind:class="{tachar: lenguaje.tachado}">
            {{ lenguaje.nombre }}
        </li>
    </ul>
</template>

<style>
    .tachar {
        text-decoration: line-through;
        color: blue;
    }
  </style>