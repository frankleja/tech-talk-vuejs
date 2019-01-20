<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <FurtherReading msg="Welcome to our VueJS tech talk"/>
    <InputBinding></InputBinding>
    <ListRendering></ListRendering>
    <DataBinding></DataBinding>
  </div>
</template>

<script>
import FurtherReading from "./components-done/FurtherReading.vue";
import DataBinding from "./components-done/DataBinding.vue";
import ListRendering from "./components-done/ListRendering.vue";
import InputBinding from "./components-done/InputBinding.vue";

export default {
  name: "app",
  components: {
    FurtherReading, 
    DataBinding,
    ListRendering,
    InputBinding
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
