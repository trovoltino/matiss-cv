<template>
  <div class="backend">
    <ul>
      <li>Laravel</li>
      <li>PHP</li>
      <li>MYSQL</li>
      
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Backend',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.logo-container {
  position: absolute;
  left: 50%;
  top: 2%;
  transform: translate(-50%, -2%);
  font-family: 'Courgette', cursive;
  font-size: 4em;
  color: rgb(3, 9, 27);
  font-weight: 700;
}
.m-logo {
  position: absolute;
  left: 50%;
  top: 2%;
  transform: translate(-50%,-2%);
}
</style>
