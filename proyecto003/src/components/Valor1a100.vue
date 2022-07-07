<script>
    export default {
        data() {
            return {
                numero: 1
            }
        }
    }
</script>

<template>
    <p>Ingrese un valor entre 1 y 100: <input type="number" v-model="numero" min="1" max="100"/></p>
    <p v-if="numero<=9">Tiene un digito</p>
    <p v-else-if="numero<=99">Tiene dos digitos</p>
    <p v-else>Tiene tres digitos</p>
</template>