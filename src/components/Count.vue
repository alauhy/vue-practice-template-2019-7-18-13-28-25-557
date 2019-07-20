<template>
    <div id="app">
        <button @click="desc" >-</button>
        <span>{{count}}</span>
        <button @click="incre">+</button>
    </div>

</template>

<script>
    export default {
        name: "HelloVue",
        data(){
            return{
                count:0
            }
        },
        methods:{
            desc:function () {
                this.count--;
                this.$emit('desc')
            },
            incre:function(){
                this.count++;
                this.$emit('incre');
            }

        }

    }



</script>

<style scoped>
    button{
        height: 30px;
        width: 40px;
        margin: 10px;

    }

</style>