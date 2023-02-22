<template>
<h1>{{ title }}</h1>
<div>
  <button @click="startPlaying" :disabled="isPlaying">Play</button>
</div>

<h1 v-if="showTimeTaken"> You took {{ this.score }} ms to complete the game</h1>

<div v-if="isPlaying">
  <Block :delay="delay" @end="endGame">
    
  </Block>
</div>

</template>

<script>
import Block from './components/Block.vue'


export default {
  name: 'App',
  components: {Block},
  data() {
    return {
      title: "Welcome to Kibs Reaction Response Game",
      isPlaying: false,
      delay: null,
      score: null,
      showTimeTaken: false,
    }
  },
  methods: {
    startPlaying(){
      this.delay= 2000 + Math.random()*5000
      this.isPlaying = true
    },
    endGame(timeTaken){
      this.isPlaying = false,
      this.score = timeTaken,
      this.showTimeTaken = true
    },
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
button {
  background: greenyellow;
  padding: 1rem;
  font-weight: bold;
  border: none;
  width: 8rem;
  border-radius: 10px;
}
</style>
