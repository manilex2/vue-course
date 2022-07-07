<script>
    export default {
        data() {
            return {
                articulos: [
                    {
                        codigo: 1,
                        descripcion: 'papas',
                        precio: 12.52
                    },
                    {
                        codigo: 2,
                        descripcion: 'naranjas',
                        precio: 21
                    },
                    {
                        codigo: 3,
                        descripcion: 'peras',
                        precio: 18.20
                    }
                ]
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
</template>