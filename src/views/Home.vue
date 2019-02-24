<template>
  <div class="home">
    <img class="bg" src="@/assets/images/bg-img.jpg" alt="">
    <transition name="switch" mode="out-in">
      <component v-bind:is="component"></component>      
    </transition>
    <button class="about-me" @click="switchComp">About Me</button>
  </div>
</template>

<script>
// @ is an alias to /src

import AboutMe from '@/components/AboutMe.vue'
import Slider from '@/components/Slider.vue'

export default {
  name: 'Home',
  components: {
    'Slider': Slider,
    'AboutMe': AboutMe
  },
  data() {
    return {
      component: 'Slider',
      showInfo: false
    }
  },
  methods: {
    switchComp() {
      if(this.component=='AboutMe') {
        this.component = 'Slider';
      } else {
        this.component = 'AboutMe';
      }
    }

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
.about-me {
  position: absolute;
  top: 80%;
  left: 50%;
  transform: translate(-50%, 0%);
  background: transparent;
  height: 50px;
  width: 130px;
  z-index: 20;
  border: 2px solid rgb(119, 119, 119);
  box-shadow: 0px 0px 10px silver;
}
.about-me:hover {
  border: 2px solid rgb(59, 59, 59);
  box-shadow: 0px 0px 10px rgb(141, 141, 141),
              0px 0px 20px rgb(110, 110, 110);
}
.about-me:active {
  background: rgb(189, 189, 189);
}
.switch-enter, .switch-leave-to {
  transition: all 0.2s ease-out;
  opacity: 0;
}
.switch-enter-to, .switch-leave {
  transition: all 0.2s ease-in;
  opacity: 1;
  
}
</style>
