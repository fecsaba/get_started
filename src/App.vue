<template>
  <div id="app">
    <button v-on:click="counter++">Increase</button>
    <button v-on:click="counter--">Decrease</button>
    <button v-on:click="secondCounter++">Increase second</button>
    <button v-on:click="secondCounter--">Decrease second</button>
    <h3>Counter: {{ counter }} | {{ secondCounter }}</h3>
    <p>Result: {{ result() }} | {{ output }}</p>

    <!--Shorthands
    v-on: - @
    v-bind - :
     -->

  </div>
</template>

<script>


export default {
  name: 'app',
  data: function() {
    return {
      counter: 0,
      secondCounter: 0
    }
  },
  computed: {
    output: function () {
      return this.secondCounter > 5 ? 'Greater 5' : 'Smaller 5'
    }
  },
  watch: {
    // eslint-disable-next-line no-unused-vars
    counter: function (value) {
      let vm = this
      setTimeout(function () {
        vm.counter = 0
      }, 2000)
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
