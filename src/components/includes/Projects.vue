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
@media only screen and (max-width: 1050px) {
  .projects {

    min-width: 360px;
    max-width: 360px;
    min-height: 360px;
    max-height: 360px;
  }
  .projects a {
    text-decoration: none;
    font-size: 16px;
    
  }
}
@media only screen and (max-width: 662px) {
  .projects {

    min-width: 320px;
    max-width: 320px;
    min-height: 320px;
    max-height: 320px;
  }
  .projects a {
    text-decoration: none;
    font-size: 14px;
    
  }
}
@media only screen and (max-width: 450px) {
  .projects {

    min-width: 260px;
    max-width: 260px;
    min-height: 260px;
    max-height: 260px;
  }
  .projects a {
    text-decoration: none;
    font-size: 12px;
  }
}

</style>
