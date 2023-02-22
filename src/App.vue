<template>
<h1>{{ title }}</h1>
<div>
  <button>Play</button>
</div>

<Block />

</template>

<script>
import Block from './components/Block.vue'


export default {
  name: 'App',
  components: {Block},
  data() {
    return {
      title: "Welcome to Kibs Reaction Response Game",
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
