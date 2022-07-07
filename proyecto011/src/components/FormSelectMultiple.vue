<script>
    export default {
        data() {
            return {
                dia: []
            }
        }
    }
</script>

<template>
    <p>
        <select v-model="dia" multiple>
            <opcion>Lunes</opcion>
            <option>Martes</option>
            <option>Miércoles</option>
            <option>Jueves</option>
            <option>Viernes</option>
            <option>Sábado</option>
            <option>Domingo</option>
        </select>
   </p>
   <p>Día seleccionado:{{ dia }}</p>
</template>