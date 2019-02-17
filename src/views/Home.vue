<template>
  <div class="home">
    <img class="bg" src="@/assets/images/bg-img.jpg" alt="">
    <Slider/>
    <Logo/>
  </div>
</template>

<script>
// @ is an alias to /src
import Logo from '@/components/Logo.vue'
import Slider from '@/components/Slider.vue'

export default {
  name: 'Home',
  components: {
    Logo,
    Slider
  }
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
  overflow: hidden;
  font-family: Verdana; 
}
.bg {
  max-width: 100%;
  min-height: 100vh;
}
</style>
