<template>
  <div class="logo">
    <div class="logo-container">
        <img class="m-logo" src="@/assets/images/main-logo.svg" alt="matiss-logo" width="200px" height="200px">
        <p class="m">MZ</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Logo',
  props: {
    msg: String
  }
}
console.log("we are in logo");
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.logo-container {
  position: absolute;
  left: 50%;
  top: 4%;
  transform: translate(-50%, -2%);
  font-family: 'Courgette', cursive;
  font-size: 4em;
  color: rgb(255, 255, 255);
  font-weight: 700;
}
.m-logo {
  position: absolute;
  left: 50%;
  top: 2%;
  transform: translate(-50%,-2%);
}
</style>
