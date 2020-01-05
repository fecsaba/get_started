<template>
  <div id="app">
    <button v-on:click="counter++">Increase</button>
    <button v-on:click="counter--">Decrease</button>
    <h3>Counter: {{ counter }}</h3>
    <p>Result: {{ result() }}</p>
  </div>
</template>

<script>


export default {
  name: 'app',
    data: function() {
      return {
        counter: 0
      }
    },
    methods: {
      result() {
        return this.counter > 5 ? 'Greater 5' : 'Smaller 5'
      }
    }
}

</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
