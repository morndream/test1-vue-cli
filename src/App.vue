<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Ev/>
    <Com :age="age" :birthday="brthday" @toParent="patch">
      <h1 slot="a">我要加点东西</h1>
      <h1 slot="b">我要加点东西</h1>
    </Com>
    <pagea/>
    <pageb/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Ev from './components/events.vue'
import Com from './components/com.vue'
import pagea from './components/a.vue'
import pageb from './components/b.vue'

import './components/n'
export default {
  name: 'app',
  components: {
    HelloWorld,
    Ev,
    Com,
    pagea,
    pageb
  },
  data(){
    return {
      age:182,
      brthday:'2010-1-1'
    }
  },
  methods:{
    patch(){
      this.age++
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
