<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld></HelloWorld>
    <FurtherReading></FurtherReading>
    <ListRendering></ListRendering>
    <InputBinding></InputBinding>
    <DataBinding></DataBinding>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import FurtherReading from './components-done/FurtherReading.vue'
import DataBinding from './components-done/DataBinding.vue'
import InputBinding from './components-done/InputBinding.vue'
import ListRendering from './components-done/ListRendering.vue'

export default {
  name: "app",
  components: {
    HelloWorld,
    FurtherReading,
    DataBinding,
    InputBinding,
    ListRendering
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
