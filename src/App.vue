<template>
  <div id="app">

    <input type="text" v-bind:placeholder="ph" @input="changeTitle">
    <p>{{ title }}</p>
    <p>{{ sayHello() }} - <a :href="link">{{google}}</a></p>
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
        google: 'Google'
      }
    },
    methods: {

        changeTitle: function (event) {
            this.title = event.target.value
        },
      sayHello: function () {
        return this.title + ' vue'
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
