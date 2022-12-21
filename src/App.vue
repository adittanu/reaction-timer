<template>
  <div class="container">
    <h1>Ninja Reaction Timer</h1>
    <button @click="start">Play</button>
  </div>
  <Block v-if="isPlaying" :delay="delay"/>
</template>

<script>
  import Block from './components/Block.vue'
  export default {
    name : 'App',
    components: {Block},
    data() {
      return{
        isPlaying: false,
        delay: null
      }
    },
    methods: {
      start(){
        this.delay = 2000 + Math.random() * 5000
        this.isPlaying = true
      }
    }
  }
</script>


<style scoped>
#app {
  font-family: Avenir, Arial, Helvetica, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #444;;
  margin-top: 60px;
}
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
</style>
