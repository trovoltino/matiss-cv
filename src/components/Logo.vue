<template>
  <div class="logo">
    <div class="logo-container">
      <!--<img class="m-logo" ref="logo" src="@/assets/images/main-logo.svg" alt="matiss-logo" width="200px" height="200px">-->
       <a href="/"></a>
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

p {
  margin: 20px;
}
.logo-container {
  position: absolute;
  left: 50%;
  bottom: -37%;
  font-family: 'Courgette', cursive;
  font-size: 5.5em;
  font-weight: 700;
}
.m {
  position: absolute;
  bottom: 50%;
  left: 50%;
  width: 600px;
  height: 300px;
  background: url('../assets/images/bg-img.jpg');
  background-clip: text;
  color: transparent;
  transform: translate(-50%, -50%);
  animation: moveBg 72s linear infinite;
}
a:hover {
  text-shadow: 0 0 2px white;
}

@keyframes moveBg {
  0%{
    background-position: 0% 89%;
  }
  100% {
    background-position: 100% 89%;
  }
}
@media screen and (max-width: 1092px) {
  .m {
    position: relative;
    width: 30px;
    height: 40px;
    font-size: 0.6em;
    color: rgb(241, 241, 241);
  }
  .logo-container {
    bottom: -3%;
    left: 50%;
    transform: translate(-110%, 0%)
  }
  a {
    display: none;
  }
}
</style>
