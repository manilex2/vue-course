<script>
    export default {
        data() {
            return {
                notas: []
            }
        },
        created: function () {
            this.$http.get('https://jsonplaceholder.typicode.com/posts').then(function (respuesta) {
                this.notas = respuesta.body;
            })
        }
    }
</script>

<template>
    <div v-for="nota in notas">
        <h1>{{ nota.title }}</h1>
        {{ nota.body }}
        <hr/>
    </div>
</template>