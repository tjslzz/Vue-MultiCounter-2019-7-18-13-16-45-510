<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h3>请输入数字  <input type="text" v-model.number="counter" v-on="sum=counter*8"></h3>
    <div v-for="item in counter" v-bind:key = "item.key">
      <count v-on:addnum="sum++" v-on:subnum="sum--"></count>
    </div>
    <h2>总数：{{sum}}</h2>
    </div>
</template>
<script>
import count from './components/count.vue';
export default {
  name: 'app',
  data:function(){
    return {
      counter : 0,
      sum:0,
    }
  },
  components : {count}
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
