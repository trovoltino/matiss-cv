<template>
    <div class="skill-wrap">
      <div v-bind:class="{ slide: moveRight }" class="slider">
        <transition name="opac" mode="out-in">
          <component v-bind:is="component"></component>
        </transition>
      </div>
      <div class="left-field">
        <h2>Some of my projects</h2>
        <p>Here is projects source codes as most frontend functional
          can be seen here.
        </p>
        <button class="move-right" @click="component = 'Project', moveRight = true">show projects</button>
      </div>
      <div class="right-field">
        <h2>better show me cv</h2>
        <p>Short descriptions of my skills,
          would not call myself proficient in all of them.
        </p>
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
p {
  text-align: center;
  max-width: 70%;
  margin: 40px auto;
}
h2 {
  text-transform: uppercase;
  font-size: 2.3em;
  font-family:monospace;
  text-shadow: 0px 0px 3px rgb(228, 228, 228),
                0px 0px 3px rgb(228, 228, 228);
}
.slider {
  margin: 0;
  position: relative;
  left: 30px;
  top: 50%;
  width: 450px;
  background: rgb(197, 197, 197);
  z-index: 3;
  transform: translate(0%,-50%);
  transition: all 1s ease-in-out;
}
.skill-wrap {
  width:960px;
  background:transparent;
  background: rgba(0, 0, 0, 0.5);
  height: 420px;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%,-30%);
  box-shadow: 0px 0px 13px 0px rgba(158,158,158,0.66);
}

.move-right, .move-left {
    text-align: center;
    text-transform: uppercase;
    border:none;
    font-weight: bold;
    border-radius: 80px;
    padding: 14px 0px;
    min-width: 140px;
    outline:none;
    font-size: 14px;
    color:white;
    background:#f89a35;
    cursor: pointer;
}
.slide {
  left: 50%;
}
.right-field {
  position: absolute;
  left: 3%;
  top: 50%;
  width: 420px;
  height: 320px;
  color: rgb(255, 253, 253);
  transform: translate(0, -50%);
}
.left-field {
  position: absolute;
  right: 3%;
  top: 50%;
  width: 420px;
  height: 320px;
  color: rgb(255, 253, 253);
  transform: translate(0, -50%);
}
.opac-enter, .opac-leave-to {
  transition: all 0.5s ease-out;
  opacity: 0;
}
.opac-enter-to, .opac-leave {
  transition: all 0.5s ease-in;
  opacity: 1;
}
</style>
