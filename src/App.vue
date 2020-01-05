<template>
  <div id="app">
    <div class="demo"
         @click="attachRed = !attachRed"
          :class="divClasses">
    </div>
    <div class="demo" :class="{red: attachRed}"></div>
    <div class="demo" :class="[color, {red: attachRed}]"></div>
    <hr>
    <input type="text" v-model="color">
  </div>
</template>

<script>


export default {
  name: 'app',
  data: function() {
  return {
    attachRed: false,
    color: 'green'
    }
  },
  computed: {
    divClasses: function () {
      return {
        red: this.attachRed,
        blue: !this.attachRed
      }
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

  .demo {
    width: 100px;
    height: 100px;
    background-color: gray;
    display: inline-block;
    margin: 10px;
  }

  .red {
    background-color: red;
  }
  .green {
      background-color: green;
    }
  .blue {
      background-color: blue;
    }

</style>
