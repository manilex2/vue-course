<script>
    export default {
        data() {
            return {
                estudios: 'Sin estudios'
            }
        }
    }
</script>

<template>
    <p>
        <input type="radio" value="Sin estudios" v-model="estudios" id="sinestudios"/>
        <label for="sinestudios">Sin estudios</label>
    </p>
    <p>
        <input type="radio" value="Primarios" v-model="estudios" id="primarios"/>
        <label for="primarios">Primarios</label>
    </p>
    <p>
        <input type="radio" value="Secundarios" v-model="estudios" id="secundarios"/>
        <label for="secundarios">Secundarios</label>
    </p>
    <p>
        <input type="radio" value="Universitarios" v-model="estudios" id="universitarios"/>
        <label for="universitarios">Universitarios</label>
    </p>
    <p>Sus estudios son: {{ estudios }}</p>
</template>