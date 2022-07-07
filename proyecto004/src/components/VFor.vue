<script>
    export default {
        data() {
            return {
                lenguajes: ['C', 'C++', 'C#', 'Java', 'Ruby', 'Kotlin']
            }
        }
    }
</script>

<template>
    <ul>
        <li v-for="lenguaje in lenguajes">{{ lenguaje }}</li>
    </ul>
</template>