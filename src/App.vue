<template>
  <div id="app">
    <router-view/>
    <div id="nav">
      <Head/>

    </div>
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
#nav {
  padding: 30px;
  position: absolute;
  bottom: 30px;
  left: 40%;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
