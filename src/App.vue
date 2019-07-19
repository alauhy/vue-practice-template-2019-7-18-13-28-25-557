<template>
  <div id="app">
 <Count v-for="n in 3"></Count>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Count from './components/Count.vue'
export default {
  name: 'app',
  components: {
   Count
  },
  data(){

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
