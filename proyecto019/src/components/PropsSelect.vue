<script>
    export default {
        props: ['idioma']
    }
</script>

<template>
    <div>
        <p v-if="idioma=='castellano'">Hola mundo</p>
        <p v-if="idioma=='ingles'">Hello world</p>
    </div>
</template>