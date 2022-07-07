<script>
    export default {
        data() {
            return {
                lenguajes: []
            }
        }
    }
</script>

<template>
    <p><input type="checkbox" v-model="lenguajes" value="C++">C++</p>
    <p><input type="checkbox" v-model="lenguajes" value="C">C</p>
    <p><input type="checkbox" v-model="lenguajes" value="C#">C#</p>
    <p><input type="checkbox" v-model="lenguajes" value="Java">Java</p>
    <p><input type="checkbox" v-model="lenguajes" value="Kotlin">Kotlin</p>
    <p><input type="checkbox" v-model="lenguajes" value="Python">Python</p>
    <p><input type="checkbox" v-model="lenguajes" value="Ruby">Ruby</p>      
    <h3>Lenguajes seleccionados</h3>
    <ul>
        <li v-for="lenguaje in lenguajes">{{ lenguaje }}</li>
    </ul>
    <p>Cantidad de lenguajes que conoce:{{ lenguajes.length }}</p>
</template>