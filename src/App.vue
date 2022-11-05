<template>
  <div id="app1">
    <p>hello World!!!!</p>
    <p>全局 count={{ count }}</p>
    <hr>
    <input type="text" ref="inpRef" v-if="flag" @blur="lostFocus"><button v-else @click="showInput">显示输入框</button>
    <div class="box">
      <Left init_msg="这是左边的部分" @countChanged="valChanged"></Left>
      <Right></Right>
    </div>
    <hr>
    <img alt="Vue logo" src="./assets/logo.png">
    <hello msg="Lichuan Welcome."></hello>
  </div>
  
</template>

<script>
import Hello from "@/components/HelloWorld.vue"
import Left from "@/components/Left.vue"
import Right from "@/components/Right.vue"

export default{
  components:{
    
    'hello' : Hello,
    Left,
    Right,
  },
  data(){
    return {
      flag:true,
      count: 0
    }
  },
  created(){
    console.log('created in APP')
  },
  mounted(){
    this.$refs.inpRef.focus()
  },
  methods:{
    valChanged(val){
      //console.log('val changed.')
      this.count = val
    },
    showInput(){
      this.flag=true
      this.$nextTick(()=>{
        this.$refs.inpRef.focus()
      })
    },
    lostFocus(){
      this.flag = false
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
