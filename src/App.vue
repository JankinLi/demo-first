<template>
  <div id="app">
    <p>hello World!!!!</p>
    <p>全局 {{ count }}</p>
    <hr>
    <left_part init_msg="这是左边的部分" @countChanged="ValChanged"></left_part>
    <hr>
    <img alt="Vue logo" src="./assets/logo.png">
    <hello msg="Lichuan Welcome."></hello>
  </div>
  
</template>

<script>
import Hello from "@/components/HelloWorld.vue"
import Left from "@/components/Left.vue"

export default{
  components:{
    'hello' : Hello,
    'left_part': Left,
  },
  data(){
    return {
      count: 0
    }
  },
  methods:{
    ValChanged(val){
      //console.log('val changed.')
      this.count = val
    }
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
