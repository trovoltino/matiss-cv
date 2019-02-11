<template>
    <div class="slider">
        <Skills/>
    </div>
</template>

<script>

import Skills from '@/components/includes/Skills.vue'

export default {
  name: 'Slider',
  props: {
    msg: String
  },
  components: {
      Skills
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.slider {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%,-50%)
}
</style>
