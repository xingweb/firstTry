<template>
  <div id="app">
    <h1>welcome to vuex-001</h1>
    <input type="button" value="增加" @click='increment'>
    <input type="button" value="减少" @click='decrement'>
    <input type="button" value="偶增" @click='odd'>
    <input type="button" value="点击异步" @click='async'>
    <div>
    现在的数字为：{{count}}, 他是  {{getodd}}
    </div>
  </div>
</template>

<script>
import {mapGetters,mapActions} from 'vuex'
export default {
    methods:mapActions([
        'increment',
        'decrement',
        'odd',
        'async'
      ]),
    computed:mapGetters([
         'count',
         'getodd'
      ])
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

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
