<script>
    export default {
        data() {
            return {
                articulos: []
            }
        },
        methods: {
            agregarArticulo: function () {
                this.articulos.push({
                    codigo: this.codigo,
                    descripcion: this.descripcion,
                    precio: this.precio
                });
                this.codigo = '';
                this.descripcion = '';
                this.precio = '';
            }
        }
    }
</script>

<template>
  <table border="1">
      <tr>
          <th>Codigo</th>
          <th>Descripcion</th>
          <th>Precio</th>
      </tr>
      <template v-for="articulo in articulos">
        <tr>
            <td>{{ articulo.codigo }}</td>
            <td>{{ articulo.descripcion }}</td>
            <td>{{ articulo.precio }}</td>
        </tr>
      </template>
  </table>
  <form v-on:submit.prevent="agregarArticulo">
    <p>Ingrese codigo: <input type="number" v-model="codigo"></p>
    <p>Ingrese descripcion: <input type="text" v-model="descripcion"></p>
    <p>Ingrese precio: <input type="text" v-model="precio"></p>
    <p><input type="submit" value="Agregar"></p>
  </form>
</template>