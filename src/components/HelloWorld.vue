<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
     <p v-if="seen">现在你又看到我了</p>
     <p v-else>你失败了</p>
     <div v-n="4"></div>
     <div :class="[a1,a2]">我借你{{money}},你还我{{a}},还剩{{b}}</div>
     <div :class="{'test-1':a3}">style object</div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return {
      seen:true,
      money:100,
      a:10,
      a1:'test-1',
      a2:'test-2',
      a3:true
    }
  },
  computed:{
    b:function(){
      return this.money-this.a
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
