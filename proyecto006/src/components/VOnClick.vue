<script>
    export default {
        data() {
            return {
                contador: 0
            }
        }
    }
</script>

<template>
    <button v-on:click="contador = contador + 1">El contador vale: {{ contador }}</button>
</template>