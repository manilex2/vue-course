<script>
    export default {
        data() {
            return {
                dias: ['Lunes', 'Martes', 'Miercoles', 'Jueves', 'Viernes', 'Sabado', 'Domingo']
            }
        }
    }
</script>

<template>
    <table border="1">
        <template v-for="dia in dias">
            <tr>
                <td>{{ dia }}</td>
            </tr>
        </template>
    </table>
</template>