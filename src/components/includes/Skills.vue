<template>
  <div class="skills">
      <div class="main-skills">
        <div class="frontend">
          <h3>Front-end skills</h3>
          <ul>
            <li>JavaScript ES6+</li>
            <li>JQuery</li>
            <li>Vue.js</li>
            <li>SASS/LESS</li>
            <li>HTML5/CSS3</li>
          </ul>
        </div>
        <div class="backend">
          <h3>Back-end skills</h3>
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

}
li {
  list-style-type: none;
}
  .skills {
    background: greenyellow;
    display: flex;
    flex-direction: column;
    max-width: 500px;
  }
  .main-skills {
    display: flex;
    margin: 20px;
  }
  .frontend, .backend{
    margin: 20px;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
  }


</style>
