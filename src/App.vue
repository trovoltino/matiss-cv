<template>
  <div id="app">
    <router-view/>
    <Head/>
    
  </div>
</template>

<script>
import Head from './components/layouts/head.vue';

export default {
  name:"app",
  components: {
    Head
  }
}
</script>

<style>
body{
  background: #e4e4e4;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

</style>
