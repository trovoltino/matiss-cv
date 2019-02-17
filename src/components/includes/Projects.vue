<template>
  <div class="projects">
     <a href="#">MageBit</a>
     <a href="#">ScandiWeb</a>
     <a href="#">CryptoApi</a>
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
  </div>
</template>


<script>
export default {
  name: 'Projects'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.projects {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
    background: transparent;
    min-width: 480px;
    max-width: 480px;
    min-height: 480px;
    max-height: 480px;
}
.projects a {
  text-decoration: none;
  font-size: 20px;
  
}

</style>
