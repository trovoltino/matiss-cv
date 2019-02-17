<template>
  <div class="logo">
    <div class="logo-container">
        <img class="m-logo" ref="logo" src="@/assets/images/main-logo.svg" alt="matiss-logo" width="200px" height="200px">
        <p class="m">MZ</p>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Logo',
  props: {
    msg: String
  },
  data() {
    return{}
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.logo-container {
  position: absolute;
  left: 50%;
  top: 4%;
  transform: translate(-50%, 0%);
  font-family: 'Courgette', cursive;
  font-size: 4em;

  font-weight: 700;
}
.m-logo {
  position: absolute;
  transform: translate(-50%, 0%);
}
.m {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 600px;
  height: 300px;
  background: url('../assets/images/bg-img.jpg');
  background-clip: text;
  color: transparent;
  transform: translate(-50%, -4%);
  animation: moveBg 72s linear infinite;
}

@keyframes moveBg {
  0%{
    background-position: 0% 89%;
  }
  100% {
    background-position: 100% 89%;
  }
}
</style>
