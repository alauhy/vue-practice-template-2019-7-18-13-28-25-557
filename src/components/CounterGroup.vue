<template>

    <div id="CounterGroup">
        <Count v-for="count in counterNum" :key="count" @incre="incre"
               @desc="desc"></Count>
    </div>


</template>

<script>
    import Count from './Count'

    export default {

        name: "CounterGroup",
        props: {
            counterNum: Number,
        },
        components: {
            Count
        },
        data() {
            return {
                totalCount: 0
            }
        },
        methods: {
            incre: function () {
                this.totalCount ++;
                this.bus.$emit('sentTotalCount',this.totalCount);
            },
            desc:function () {
                this.totalCount --;
                this.bus.$emit('sentTotalCount',this.totalCount);

            }
        }
    }
</script>

<style scoped>

</style>