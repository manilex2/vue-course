<script>
    export default {
        data() {
            return {
                valor: Math.trunc(Math.random() * 6) + 1
            }
        }
    }
</script>

<template>
    <span style="display:inline-block; background-color:black; color:white; border-radius:5px;width:2rem; font-size:2rem;text-align:center">
        {{valor}}
    </span>
</template>