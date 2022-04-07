<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png" width="25%" /> -->
    <!-- <HelloWorld msg="Hello Vue in CodeSandbox!"/> -->
    <CanvasCard></CanvasCard>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld";
import CanvasCard from "./components/CanvasCard";

export default {
  name: "App",
  components: {
    // HelloWorld,
    CanvasCard,
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
