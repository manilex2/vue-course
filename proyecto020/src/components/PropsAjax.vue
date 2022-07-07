<script>
    export default {
        props: ["articulos"]
    }
</script>

<template>
    <div>
        <table border="1">
            <tr>
                <th>Código</th>
                <th>Descripción</th>
                <th>Precio</th>
            </tr>
            <tr v-for="art in articulos">
                <td>{{ art.codigo }}</td>
                <td>{{ art.descripcion }}</td>
                <td>{{ art.precio }}</td>
            </tr>
        </table>
    </div>
</template>