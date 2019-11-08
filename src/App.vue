<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <router-view/>
    <div>{{message}}</div>
    <div>
      <ul>
        <li v-for='item in movie' :key="item">{{item}}</li>
      </ul>
    </div>
    <div>
      <button @click="count--">-</button>{{count}}<button @click="count++">+</button>
    </div>
    <div>
      {{number1 + '' + number2}}   {{number2*3}}
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return{
      message:'你好',
      movie:['星际穿越','aaaaaa','bbbbbb','cccccc'],
      count:0,
      number1:4,
      number2:6
    }
  },
  methods:{
    decade:function(){
      this.count--
    },
    add:function(){
      this.count++
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
