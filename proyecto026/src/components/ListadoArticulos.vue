<script>
import ItemArticulo from './ItemArticulo.vue';

export default {
    props: ["articulos"],
    components: { ItemArticulo },
}
</script>

<template>
    <div>
        <ItemArticulo v-for="art in articulos" :articulo="art"></ItemArticulo>
    </div>
</template>