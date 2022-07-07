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
                }
            },
            decrementar: function () {
                if (this.cant > this.minimo) {
                    this.cant--;
                }
            }
        }
    }
</script>

<template>
    <div>
        <span style="width: 1rem; display: inline-block; background: #ff0">{{ cant }}</span>
        <button v-on:click="incrementar()">+</button>
        <button v-on:click="decrementar()">-</button>
    </div>
</template>