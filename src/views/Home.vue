<template>
  <div class="home">
    
    <Slider/>
    <Logo/>
  </div>
</template>

<script>
// @ is an alias to /src
import Logo from '@/components/Logo.vue'
import Slider from '@/components/Slider.vue'

export default {
  name: 'logo',
  components: {
    Logo,
    Slider
  }
}
</script>
