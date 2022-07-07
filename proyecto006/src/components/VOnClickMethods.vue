<script>
    export default {
        data() {
            return {
                contador: 0
            }
        },
        methods: {
            incrementar: function () {
                this.contador = this.contador + 1;
            }
        }
    }
</script>

<template>
    <button v-on:click="incrementar">El contador vale: {{ contador }}</button>
</template>