<script>
    export default {
        props: ['foto']
    }
</script>

<template>
    <div>
        <img :src="foto" style="border-radius: 50%;">
    </div>
</template>