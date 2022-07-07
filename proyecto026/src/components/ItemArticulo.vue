<script>
export default {
    props: ['articulo']
}
</script>

<template>
    <div>
        <p>Código: {{ articulo.codigo }}</p>
        <p>Descripción: {{ articulo.descripcion }}</p>
        <p>Precio: {{ articulo.precio }}</p><hr>
    </div>
</template>