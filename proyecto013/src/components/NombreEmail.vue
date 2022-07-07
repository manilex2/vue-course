<script>
    export default {
        data() {
            return {
                nombre: ''
            }
        },
        computed: {
            email: function () {
                if (this.nombre.length > 0) {
                    return this.nombre + '@totalmail.com';
                } else {
                    return '';
                }
            }
        }
    }
</script>

<template>
    <p>Ingrese nombre:<input type="text" v-model="nombre"></p>
    <p>email propuesto:{{ email }}</p>
</template>