<template>
  <div id="app">
    <h1 v-once>{{ title }}</h1>
    <input type="text" v-bind:placeholder="ph" @input="changeTitle">
    <p>{{ title }}</p>
    <p>{{ sayHello() }} - <a :href="link">{{google}}</a></p>
    <hr>
    <p>{{ finishedLink }}</p>
    <p v-html="finishedLink"> </p>
    <hr>
    <button v-on:click="increase(2, $event)">Click me</button>
    <h3>{{ counter }}</h3>
    <p v-on:mousemove="updateCoordinates">
      Coordinates: {{ x }} / {{ y }} - <span v-on:mousemove="dummy">DEAD-SPOT</span></p>
    </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
    data() {
      return {
          title: 'Hello',
        ph: 'Write here any',
        link: 'https://google.com',
        google: 'Google',
        finishedLink: '<a href="http://google.com">Google</a>',
        counter: 0,
        x: 0,
        y: 0
      }
    },
    methods: {

        changeTitle: function (event) {
            this.title = event.target.value
        },
      sayHello: function () {
          this.title = 'Hi'
        return this.title + ' vue'
      },
      increase: function(step, event) {
          this.counter += step
        // eslint-disable-next-line no-console
        console.log(event)
      },
      updateCoordinates: function(event) {
          this.x = event.clientX
          this.y = event.clientY
      },
      dummy: function(event) {
          event.stopPropagation()
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
