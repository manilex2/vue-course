<script>
    export default {
        data() {
            return {
                psw: '',
                repPsw: ''
            }
        }
    }
</script>

<template>
    <p>Ingrese su contraseña: <input type="password" v-model="psw"/></p>
    <p>Repita su contraseña: <input type="password" v-model="repPsw"/></p>
    <p v-if="psw === repPsw">Las contraseñas son iguales</p>
    <p v-else>Las contraseñas son diferentes</p>
</template>