<template>
<h1>{{ title }}</h1>
<div>
  <button @click="startPlaying">Play</button>
</div>

<div v-if="isPlaying">
  <Block>
    
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
    }
  },
  methods: {
    startPlaying(){
      this.delay = 2000 + Math.random() *5000
      this.isPlaying = true

      console.log(this.delay)
    }
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
