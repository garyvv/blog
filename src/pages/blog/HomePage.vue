<template>
  <el-container>
    <el-header><Header /></el-header>
    <el-main><h1>{{ msg }}</h1></el-main>
    <el-footer>Footer</el-footer>
  </el-container>
</template>

<script>
import Header from '@/components/BlogHeader'
export default {
  name: 'HomePage',
  data () {
    return {
      msg: 'Welcome to Gary\'s Blog'
    }
  },
  components: {
    Header
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
.el-header {
  padding: 0;
}
</style>
