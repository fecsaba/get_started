<template>
  <div id="app">
    <div class="demo" :style="{backgroundColor: color}"></div>
    <div class="demo" :style="myStyle"></div>
    <div class="demo" :style="[myStyle, {height: width + 'px'}]"></div>
    <hr>
    <input type="text" v-model="color">
    <br>
    <input type="text" v-model="width">
  </div>
</template>

<script>


export default {
  name: 'app',
  data: function() {
  return {
    color: 'gray',
    width: 100
    }
  },
  computed: {
    myStyle: function () {
      return {
        backgroundColor: this.color,
        width: this.width + 'px'
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

  /*.red {*/
  /*  background-color: red;*/
  /*}*/
  /*.green {*/
  /*    background-color: green;*/
  /*  }*/
  /*.blue {*/
  /*    background-color: blue;*/
  /*  }*/

</style>
