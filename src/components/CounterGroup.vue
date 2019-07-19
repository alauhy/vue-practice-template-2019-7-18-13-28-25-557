<template>

    <div id="CounterGroup">
        <Count v-for="count in counterNum" :key="count"></Count>
    </div>


</template>

<script>
    import Count from './Count'

    export default {

        name: "CounterGroup",
        props:{
            counterNum:Number
        },
        components: {
            Count
        },
        data() {
            return {
            }
        }
    }
</script>

<style scoped>

</style>