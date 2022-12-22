<template>
    <h1>Your score is {{ score }}</h1>
    <p class="rank">{{ rank }}</p>
</template>

<script>
    export default {
        props: ['score'],
        data() {
            return {
                rank: null
            }
        },
        mounted() {
            if(this.score < 250) {
                this.rank = 'Ninja Fingers'
            } else if (this.score < 400) {
                this.rank = 'Rapid Reflexes'
            } else {
                this.rank = 'Snail Pace...'
            }
        }
    }
    
</script>

<style scoped>
    h1 {
        font-size: medium;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
        line-height: 8px;
        color: slateblue;
    }

    .rank {
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>