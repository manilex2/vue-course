<script>
    export default {
        data() {
            return {
                articulos: [
                    {
                        codigo: 1, 
                        descripcion: 'papas',
                        precio: 12.52
                    },{
                        codigo: 2, 
                        descripcion: 'naranjas',
                        precio: 21
                    },{
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
    <div>
        <table border="1">
            <tr>
                <td>Código</td>
                <td>Descripción</td>
                <td>Precio</td>
            </tr>
            <tr v-for="art in articulos"><td>{{art.codigo}}</td><td>{{art.descripcion}}</td><td>{{art.precio}}</td></tr>
        </table>
    </div>
</template>