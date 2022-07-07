<script>
    export default {
        data() {
            return {
                comentarios: ''
            }
        }
    }
</script>

<template>
    <p><textarea v-model="comentarios" cols="100" rows="5" maxlength="200"></textarea></p>
    <p>Cantidad de caracteres ingresados: {{ comentarios.length }}</p>
</template>