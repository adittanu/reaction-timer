<template>
    <h1>Your score is {{ score }}</h1>
</template>

<script>
    export default {
        props: ['score']
    }
</script>

<style scoped>
    h1 {
        font-size: medium;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
        line-height: 8px;
        color: slateblue;
    }
</style>