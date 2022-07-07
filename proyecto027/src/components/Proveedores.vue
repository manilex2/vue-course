<script>
    export default {
        data() {
            return {
                proveedores: [
                    {
                        nombre: 'Martinez, luis',
                        direccion: 'Colon 123'
                    },{
                        nombre: 'Rodriguez, ana',
                        direccion: 'Pringles 534'
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
                <td>Nombre</td>
                <td>Dirección</td>
            </tr>
            <tr v-for="prov in proveedores">
                <td>{{prov.nombre}}</td>
                <td>{{prov.direccion}}</td>
            </tr>
        </table>
   </div>
</template>