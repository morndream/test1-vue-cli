<template>
  <div>
        <slot name="a"></slot>
   child components
    {{name}}
    {{age}}
    <p>{{birthday}}</p>
    <div @click="toParent">子组件传值给父组件</div>
    <slot name="b"></slot>
  </div>
</template>
<script>
export default {
  props:['age','birthday'],
  data(){
    return{
      name:'com'
    }
  },
  methods:{
    toParent(){
      this.$emit('toParent')
    }
  }
}
</script>
<style scoped>
  
</style>