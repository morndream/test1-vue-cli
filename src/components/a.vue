<template>
  <div>
    pagea {{this.$store.state.money.money}}
    <button @click="add">增加</button>
    <button @click="reduce">删减</button>
  </div>
</template>
<script>
import {mapActions} from 'vuex'
export default {
  methods:{
   ...mapActions('money',['add','reduce'])
  },
  data(){
    return {

    }
  }
}
</script>
<style scoped>
  
</style>