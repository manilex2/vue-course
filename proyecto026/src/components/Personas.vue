<script>
import FotoPersona from './FotoPersona.vue';

export default {
    props: ["datos"],
    components: { FotoPersona }
}
</script>

<template>
    <div>
        <p v-for="dato in datos">
            Nombre: {{ dato.name.first }}, {{ dato.name.last }}<br/>
            <FotoPersona :foto="dato.picture.large"></FotoPersona>
        </p>
    </div>
</template>