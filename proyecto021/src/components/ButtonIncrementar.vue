<script>
    export default {
        data() {
            return {
                cantidad: 0
            }
        },
        methods: {
            incrementar: function () {
                this.cantidad++;
            }
        }
    }
</script>

<template>
    <div>
        <button v-on:click="incrementar()">{{cantidad}}</button>
    </div>
</template>