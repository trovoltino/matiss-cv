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
@media only screen and (max-width: 1050px) {
  ul {
    justify-content:space-evenly;
  }
  li {
    font-size: 14px;
  }
  h3 {
    font-size: 18px;
  }
  .skills {
    align-items: center;
    min-width: 260px;
    min-height: 340px;
    max-height: 340px;
  }
  .main-skills {
    margin-top:30px;
  }
}
@media only screen and (max-width: 760px) {
  ul {
    justify-content:space-evenly;
  }
  li {
    font-size: 14px;
  }
  h3 {
    font-size: 20px;
  }
  .skills {
    align-items: center;
    min-width: 280px;
    min-height: 340px;
    max-height: 340px;
  }
  .main-skills {
    margin-top:20px;
  }
}
@media only screen and (max-width: 450px) {
  ul {
    display: flex;
    flex-direction: column;
    justify-content:space-evenly;
    padding: 0;
    margin: 0;
  }
  li {
    font-size: 12px;
    font-weight: bold;
    list-style-type: none;
  }
  h3 {
    font-size: 16px;
    font-family:Verdana ;
    text-transform: uppercase;
  }
  .skills {
    background: transparent;
    display: flex;
    flex-direction: column;
    align-items: center;
    min-width: 260px;
    min-height: 300px;
    max-height: 300px;
  }
  .main-skills {
    margin-top:20px;
  }
}
@media only screen and (max-width: 380px) {
  ul {
    display: flex;
    flex-direction: column;
    justify-content:space-evenly;
    padding: 0;
    margin: 0;
  }
  li {
    font-size: 10px;
    font-weight: bold;
    list-style-type: none;
  }
  h3 {
    font-size: 14px;
    font-family:Verdana ;
    text-transform: uppercase;
  }
  .skills {
    background: transparent;
    display: flex;
    flex-direction: column;
    align-items: center;
    min-width: 260px;
    min-height: 300px;
    max-height: 300px;
  }
  .main-skills {
    margin-top:20px;
  }
}

</style>
