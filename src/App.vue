<template>
  <div id="app">
    <p>hello</p>
    <hr>
    <img alt="Vue logo" src="./assets/logo.png"></img>
    <hello msg="Lichuan Welcome."></hello>
  </div>
  
</template>

<script>
import Hello from "@/components/HelloWorld.vue"

export default{
  components:{
    'hello' : Hello,
  }
}
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
