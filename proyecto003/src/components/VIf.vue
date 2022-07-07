<script>
    export default {
        data() {
            return {
                edad: 0
            }
        }
    }
</script>

<template>
    <p>Ingrese una edad: <input type="number" v-model="edad"/></p>
    <p v-if="edad>=18">Es mayor de edad.</p>
</template>