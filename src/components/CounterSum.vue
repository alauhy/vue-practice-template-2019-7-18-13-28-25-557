<template>
    <span>{{totalCount}}</span>
</template>

<script>
        export default {
        name: "CounterSum",
        data(){
            return{
                totalCount: 0
            }
        },
        created() {
            this.bus.$on('sentTotalCount',(data)=>{
                this.totalCount = data;
            })
        }
    }
</script>

<style scoped>

</style>