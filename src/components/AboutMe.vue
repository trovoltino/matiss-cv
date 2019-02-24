<template>
  <div class="about">
    <div class="picture">
      <!--<img class="m-logo" ref="logo" src="@/assets/images/main-logo.svg" alt="matiss-logo" width="200px" height="200px">-->
       
    </div>
    <p class="info">
        I am developer who enjoys working with latest technology such as VueJs,
        in free time I am trying to further my knowlage of given framework and 
        develop basic aps and functionals to get better understanding of inner workings
        and capabilitys of vuejs. In current work requires usage CMS (magento2), 
        and heavy usage of jquery.
    </p>
  </div>
</template>

<script>

export default {
  name: 'AboutMe',
  data() {
    return{}
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.about {
    font-size: 1.3em;
    height: 500px;
    width: 800px;
    background: rgba(0, 0, 0, 0.5);
    color: white;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -65%);
    box-shadow: 0px 0px 13px 0px rgba(158,158,158,0.66);       
}
.info {
    padding: 20px;
    margin: 20px;
}

</style>