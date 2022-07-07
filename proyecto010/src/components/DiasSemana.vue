<script>
    export default {
        data() {
            return {
                dias: []
            }
        }
    }
</script>

<template>
    <p><input type="checkbox" v-model="dias" value="Lunes">Lunes</p>
    <p><input type="checkbox" v-model="dias" value="Martes">Martes</p>
    <p><input type="checkbox" v-model="dias" value="Miércoles">Miércoles</p>
    <p><input type="checkbox" v-model="dias" value="Jueves">Jueves</p>
    <p><input type="checkbox" v-model="dias" value="Viernes">Viernes</p>
    <p><input type="checkbox" v-model="dias" value="Sábado">Sábado</p>
    <p><input type="checkbox" v-model="dias" value="Domingo">Domingo</p>
    <p v-if="dias.length < 5" style="color:red">Debe seleccionar por lo menos 5 días</p>
    <h3>Días seleccionados</h3>
    <ul>
        <li v-for="dia in dias">{{ dia }}</li>
    </ul>
</template>