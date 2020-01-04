<template>
  <div id="app">

    <input type="text" :placeholder="ph" @input="changeTitle">
    <p>{{ title }}</p>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
    data() {
      return {
          title: 'Hello',
        ph: 'Write here any'
      }
    },
    methods: {

        changeTitle: function (event) {
            this.title = event.target.value
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
