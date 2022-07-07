<script>
    export default {
        props: ['valor', 'minimo', 'maximo'],
        data() {
            return {
                cant: this.valor
            }
        },
        methods: {
            incrementar: function () {
                if (this.cant < this.maximo) {
                    this.cant++;
                    this.$emit('incremento');
                }
            },
            decrementar: function () {
                if (this.cant > this.minimo) {
                    this.cant--;
                    this.$emit('decremento');
                }
            }
        }
    }
</script>

<template>
    <div>
        <span style="width: 1rem; display: inline-block; background: #ff0">{{cant}}</span>
        <button @click="incrementar()">+</button>
        <button @click="decrementar()">-</button>
    </div>
</template>