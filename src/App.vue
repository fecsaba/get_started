<template>
  <div id="app">
    <input type="text" v-model="name"/>
    <p>{{ name }}</p>

  </div>
</template>

<script>


export default {
  name: 'app',
    data: function() {
    return {
        name: 'Rob'
      }
    },
    methods: {

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
