<template>
    <div class="skill-wrap">
      <transition name="fade">
        <div class="slider" v-if="moveRight">
          <component v-bind:is="component"></component>
        </div>
      </transition>
        <button class="btn1" @click="component = 'Project', moveRight = !moveRight">Want to see projects</button>
        <button class="btn2" @click="component = 'Skill'">Back to CV</button>
    </div>
</template>

<script>

import Skills from '@/components/includes/Skills.vue'
import Projects from '@/components/includes/Projects.vue'

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
    position: absolute;
    left: 30%;
    top: 50%;
    background: purple;
    transform: translate(-50%,-50%)
}
.skill-wrap {
  width:80%;
  background: blue;
  height: 40vh;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%,-50%)
}
.btn1, .btn2 {
  position: relative;
  top: 130%;
}
</style>
