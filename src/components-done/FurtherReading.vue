<template>
  <div class="hello">
    <h1>{{ msg }}</h1>  
    <h2>Vue further reading</h2>
    <ul>
      <li><a href="https://medium.com/vue-mastery" target="_blank" rel="noopener">Vue Mastery</a></li>
      <li><a href="https://cli.vuejs.org/guide/installation.html" target="_blank" rel="noopener">Vue CLI</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "FurtherReading",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
