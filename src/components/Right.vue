<template>
  <div id="right">
    <p>这是右边的部分</p>
    <hr>
    <p>{{ count }}</p>
  </div>
</template>

<script>
export default {
    data(){
        return {
            count: 1
        }
    }
}
</script>

<style lang="less" scoped>
    #right{
        padding:0 20px 20px;
        background-color: aqua;
        font-size: 20px;
        min-height: 300px;
        width:50%;
        flex:1;
    }
</style>