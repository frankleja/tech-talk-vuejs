<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <FurtherReading msg="Welcome to our VueJS tech talk"/>
  </div>
</template>

<script>
import FurtherReading from "./components/FurtherReading.vue"

export default {
  name: "app",
  components: {
    FurtherReading
}
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
