<template>
    <div class="skill-wrap">
      <div v-bind:class="{ slide: moveRight }" class="slider">
        <transition name="opac" mode="out-in">
          <component v-bind:is="component"></component>
        </transition>
      </div>
      <div class="left-field">
        <button class="move-right" @click="component = 'Project', moveRight = true">Want to see projects</button>
      </div>
      <div class="right-field">
        <button class="move-left" @click="component = 'Skill', moveRight = false">Back to CV</button>
      </div>
      
      
    </div>
</template>

<script>

import Skills from '@/components/includes/Skills.vue'
import Projects from '@/components/includes/Projects.vue'
import ('@/assets/js/slide.js');

export default {
  name: 'Slider',
  components: {
    'Skill': Skills,
    'Project': Projects
  },
  data() {
    return {
      component: 'Skill',
      moveRight: false,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.slider {
  margin: 0;
  position: relative;
  left: 30px;
  top: 50%;
  width: 450px;
  background: rgb(184, 255, 228);
  z-index: 3;
  transform: translate(0%,-50%);
  transition: all 2s ease-in-out;
}
.skill-wrap {
  width:960px;
  background: blue;
  height: 420px;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%,-50%);
}

.move-right {
  
}

.opac-enter, .opac-leave-to {
  transition: all 1s ease-out;
  opacity: 0;
}
.opac-enter-to, .opac-leave {
  transition: all 1s ease-in;
  opacity: 1;
}
.slide {
  left: 50%;
}
.right-field {
  display: block;
  position: absolute;
  left: 0;
  top: 0;
  background: red;
  width: 480px;
  height: 300px;
}
.left-field {
  display: block;
  position: absolute;
  right: 0;
  top: 0;
  background: rgb(248, 233, 20);
  width: 480px;
  height: 300px;
}
</style>
