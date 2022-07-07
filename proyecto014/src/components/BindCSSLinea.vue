<script>
    export default {
        data() {
            return {
                tamañoFuente: 20,
                colorParrafo: '#000'
            }
        }
    }
</script>

<template>
    <p>Tamaño de la fuente: <input type="range" v-model="tamañoFuente" min=10 max=100>{{ tamañoFuente }} </p>
    <p>Color: <input type="color" v-model="colorParrafo"></p>      
    <p v-bind:style="{'font-size':tamañoFuente + 'px', 'color': colorParrafo}">Párrafo de prueba</p>
</template>