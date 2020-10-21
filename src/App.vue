<template>
  <div id="app">
    <div id="sketch"></div>
    <div class="title"> &lt;ROBO-EXPO/&gt; </div>
    <div class="about">
      Most of the organizations often realize the design flaws during the manufacturing stage. This may force them to revisit the design phase again. <b>CAD</b> modelling increases the overall accuracy of the design and eliminates the need for redundant designs.
      <br/>
      <br/>
      Visit <a class="link" href="https://robotics-club-iiitdmj.github.io/ROBO-EXPO/">README.md</a> to get started.
    </div>
    <Grid />
  </div>
</template>

<script>
import Grid from './components/Grid.vue';
import P5 from "p5";
import '../public/sketch.js'

export default {
  name: 'App',
  components: {
    Grid,
  },
  created(){
    const p = new P5();
  }
};
</script>

<style>

@font-face{
    font-family: 'JetBrains Mono';
    src: url('https://raw.githubusercontent.com/JetBrains/JetBrainsMono/master/fonts/web/JetBrainsMono-Regular.woff2') format('woff2'),
         url('https://raw.githubusercontent.com/JetBrains/JetBrainsMono/master/fonts/web/JetBrainsMono-Regular.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}

body {
  background: #000000;
  color: rgb(209, 209, 209);
}

.title {
  font-size: 64px;
  text-align: center;
  color: #ffffff;
  letter-spacing: -5px;
}

.about {
  font-size: 22px;
  text-align: center;
  color: #e0e0e0;
}

a {
  color: inherit;
  transition: all .2s ease;
}

a:hover{
  color: #fff;
}

#app {
  font-family: 'JetBrains Mono', 'Monospace';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: 10% 5%;
  text-rendering:optimizeLegibility;
}
</style>
