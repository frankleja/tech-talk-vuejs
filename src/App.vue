<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to our VueJS tech talk"/>
    <DataBinding></DataBinding>
    <ListRendering></ListRendering>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import DataBinding from "./components/DataBinding.vue";
import ListRendering from "./components/ListRendering.vue";

export default {
  name: "app",
  components: {
    HelloWorld, 
    DataBinding,
    ListRendering
  }
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
