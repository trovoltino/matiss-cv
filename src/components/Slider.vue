<template>
    <div class="main">
      <div class="skill-wrap">
        <div v-bind:class="{ slide: moveRight }" class="slider">
          <transition name="opac" mode="out-in">
            <component v-bind:is="component"></component>
          </transition>
        </div>
        <div class="field-wrap">
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
      </div>
      <logo/>
    </div>

</template>

<script>

import Skills from '@/components/includes/Skills.vue'
import Projects from '@/components/includes/Projects.vue'
import Logo from '@/components/Logo.vue'
import ('@/assets/js/slide.js');

export default {
  name: 'Slider',
  components: {
    'Logo': Logo,
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
  font-family: Verdana; 
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
  width: 480px;
  height: 480px;
  background: url(../assets/images/full-moon.jpg);
  background-position: center;
  border-radius: 50%;
  box-shadow: 0px 0px 20px silver,
              0px 0px 30px silver,
              0px 0px 40px silver;
  z-index: 3;
  transform: translate(0%,-50%);
  transition: all 1s ease-in-out;
}
.skill-wrap {
  width:1020px;
  background:transparent;
  background: rgba(0, 0, 0, 0.5);
  height: 420px;
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%,-70%);
  box-shadow: 0px 0px 13px 0px rgba(158,158,158,0.66);
}

.move-right, .move-left {
    text-align: center;
    text-transform: uppercase;
    border:solid 0px rgb(235, 235, 235);
    font-weight: bold;
    border-radius: 80px;
    padding: 18px 0px;
    min-width: 160px;
    outline:none;
    font-size: 14px;
    color:white;
    background: #f89a35;
    cursor: pointer;
}
.move-left:hover, .move-right:hover {
  background:#f1830e;
}
.move-left:active, .move-right:active {
  background:#a05709;
}
.slide {
  left: 50%;
}
.field-wrap {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 100%;
  display: flex;
  flex-direction: row-reverse;
  justify-content: space-around;
  transform: translate(-50%, -50%);
}
.right-field {
  width: 420px;
  height: 320px;
  color: rgb(255, 253, 253);
}
.left-field {
  width: 420px;
  height: 320px;
  color: rgb(255, 253, 253);
}
.opac-enter, .opac-leave-to {
  transition: all 0.5s ease-out;
  opacity: 0;
}
.opac-enter-to, .opac-leave {
  transition: all 0.5s ease-in;
  opacity: 1;
}
@media screen and (max-width: 1092px) {
  .field-wrap {
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
  }
  .skill-wrap {
  width:70%;
  height: 80%;
  transform: translate(-50%,-50%);
  }
  
  .slider {
  display: none;
  position: relative;
  left: 50%;
  bottom: 0%;
  width: 420px;
  height: 420px;
  background: url(../assets/images/full-moon.jpg);
  background-position: center;
  border-radius: 50%;
  box-shadow: 0px 0px 20px silver,
              0px 0px 30px silver,
              0px 0px 40px silver;
  z-index: 3;
  transform: translate(-50%,0%);
  transition: all 1s ease-in-out;
  }
}
</style>
