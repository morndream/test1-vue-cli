<template>
  <div class="vuex">
   vuex {{$store.state.count}}
   <button type="button" name="button" @click="increment">增加</button>
   <button type="button" name="button" @click="decrement">删减</button>
   <button @click="show">点击</button>
  </div>
</template>
<script>
import {mapActions} from 'vuex'
export default {
  methods:{
    ...mapActions(['increment','decrement']),
    show(){
      console.log(111)
    }
  },
  data(){
    return {}
  }
}
</script>
<style scoped>
  
</style>