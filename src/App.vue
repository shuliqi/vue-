<template>
  <div id="app">
    <parent></parent>
  </div>
</template>

<script>
// import parent from "./components/parent"; // props/$emit方式
// import parent from './components/parent|children/parent'
// import parent from "./components/provide|inject/A";
// import parent from "./components/ref|$refs/parent";
// import parent from "./components/eventBus/A"
import parent from "./components/$attrs|$listeners/A"
export default {
  name: 'App',
  components: {
    parent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
