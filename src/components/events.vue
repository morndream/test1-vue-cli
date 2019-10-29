<template>
  <div class="events">
    <button type="button" name="button" @click="msg('s',$event)">test</button>
    <div @click="parent"> 
       parent
      <div @click.stop="child">child</div>
    </div>
 </div>
</template>
<script>
export default {
  data(){
    return {}
  },
  methods:{
    msg(a,b){
      window.console.log(Math.random(),a,b)
    },
    parent(){
      window.console.log("parent")
    },
    child(){
      window.console.log("child")
    }
  }
}
</script>
<style scoped>
  
</style>