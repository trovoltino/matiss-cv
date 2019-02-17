<template>
  <div class="skills">
      <div class="main-skills">
        <div class="frontend">
          <h3>Front-end</h3>
          <ul>
            <li>JavaScript ES6+</li>
            <li>JQuery</li>
            <li>Vue.js</li>
            <li>SASS/LESS</li>
            <li>HTML5/CSS3</li>
          </ul>
        </div>
        <div class="backend">
          <h3>Back-end</h3>
          <ul>
            <li>Laravel</li>
            <li>PHP</li>
            <li>MYSQL</li>
          </ul>
        </div>
      </div>
      <div class="random">
        <h3>Other Skills</h3>
        <ul>
          <li>VB.NET</li>
          <li>Magento2</li>
          <li>Gulp</li>
          <li>Basic PhotoShop</li>
          <li>Windows/Linux</li>
          <li>Responsive Design</li>
        </ul>
      </div>
  </div>
</template>


<script>
export default {
  name: 'Skills'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 0;
  margin: 0;
}
li {
  font-size: 16px;
  font-weight: bold;
  list-style-type: none;
}
h3 {
  font-size: 22px;
  font-family:Verdana ;
  text-transform: uppercase;
}
  .skills {
    background: transparent;
    display: flex;
    flex-direction: column;
    min-width: 480px;
    max-width: 480px;
    min-height: 480px;
    max-height: 480px;
  }
  .main-skills {
    display: flex;
    justify-content: space-evenly;
    align-items: flex-start;
    margin: 5px 5px;
    margin-top: 40px;
  }
  .frontend, .backend{
    margin: 10px;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
  }


</style>
