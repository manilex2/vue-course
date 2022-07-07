<script>
    export default {
        data() {
            return {
                articulos: []
            }
        },
        methods: {
            recuperarArticulos: function () {
                this.$http.get('http://scratchya.com.ar/vue/datos.php').then(function (respuesta) {
                    this.articulos=respuesta.body
                })
            }
        }
    }
</script>

<template>
    <button v-on:click="recuperarArticulos()">Recuperar artículos</button>
    <table border="1">
        <tr>
            <th>Código</th>
            <th>Descripción</th>
            <th>Precio</th>
        </tr>
        <tr v-for="articulo in articulos">
          <td>{{ articulo.codigo }}</td>
          <td>{{ articulo.descripcion }}</td>
          <td>{{ articulo.precio }}</td>
        </tr>
        </table>
</template>