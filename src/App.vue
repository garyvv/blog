<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body {
  margin: 0;
}
header {
  height: auto !important;
}
.el-header {
  padding: 0;
}
.el-main {
  padding: 0;
}
.el-footer {
  padding: 0;
  margin-bottom: 0;
  margin-top: 20px;
  width: 100%;
  text-align: center;
  height: 0 !important;
}
a {
  color: #42b983;
  text-decoration:none;
}
</style>
