<template>
    <div id="app">
        <input type="number" v-model="counterNum">
        <CounterGroup :counterNum="parseInt(counterNum)"></CounterGroup>
        <CounterSum></CounterSum>
    </div>
</template>

<script>
    import CounterSum from './components/CounterSum'
    import CounterGroup from './components/CounterGroup'

    export default {
        name: 'app',

        components: {
            CounterGroup,
            CounterSum
        },
        data() {
            return {
                counterNum: 2
            }
        }
    }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
