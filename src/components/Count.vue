<template>
    <div id="app">
        <button v-on:click="desc" >-</button>
        <span>{{count}}</span>
        <button v-on:click="incre">+</button>
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
            desc(){
                this.count--
            },
            incre(){
                this.count++
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