<script>
    export default {
        props: ['minimo', 'maximo'],
        data() {
            return {
                numero: Math.trunc(Math.random() * (this.maximo + 1 - this.minimo) + this.minimo)
            }
        }
    }
</script>

<template>
    <div>
        <slot :numero="numero">{{ numero }}</slot>
    </div>
</template>