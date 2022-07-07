<script>
    export default {
        data() {
            return {
                tipo: Math.trunc(Math.random() * 4), 
                valor: Math.trunc(Math.random() * 6) + 1,
                nombre: ['pica', 'corazon', 'diamante', 'trébol']
            }
        }
    }
</script>

<template>
    <span style="display:inline-block; background-color:black; color:white; border-radius:5px; width:8rem; height:13rem; font-size:2rem; text-align:center">
        {{valor}}<br/>
        {{nombre[tipo]}}
    </span>
</template>