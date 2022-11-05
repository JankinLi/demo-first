<template>
    <dir id="left">
        <h1>This is Left side.</h1>
        <h4>{{ message }}</h4>
        <h4>{{ count }}</h4>
        <button @click="add">click me</button>
    </dir>
</template>

<script>
export default {
    props:{
        init_msg:{
            default: 'Lichuan'
        },
    },
    data(){
        return {
            message: this.init_msg,
            count:0,
        }        
    },
    methods:{
        add(){
            this.count += 1;
            this.$emit('countChanged', this.count)
        }
    }
}
</script>

<style lang="less" scoped>
    #left{
        padding:0 20px 20px;
        background-color: pink;
        min-height: 300px;
        width:50%;
        flex:1;
    }
</style>