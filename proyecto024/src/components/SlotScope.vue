<script>
    export default {
        data() {
            return {
                dias: ['lunes', 'martes', 'miércoles', 'jueves', 'viernes', 'sábado', 'domingo']
            }
        }
    }
</script>

<template>
    <div>
        <slot v-for="dia in dias" :nombre="dia">{{ dia }}-</slot>
    </div>
</template>