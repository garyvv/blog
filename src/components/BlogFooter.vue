<template>
  <a href="http://www.miitbeian.gov.cn" target="_blank">
    <el-alert
      title="粤ICP备16012388号"
      type="info"
      center
      :closable="false">
    </el-alert>
  </a>
</template>

<script>
export default {
  name: 'BlogHeader',
  data () {
    return {
      menu: [
        {
          'id': '1',
          'name': '首页',
          'class': 'bg-purple',
          'icon': 'el-icon-menu',
          'link': '/',
        },
        {
          'id': '2',
          'name': 'GitHub',
          'class': 'bg-purple',
          'icon': 'el-icon-star-on',
          'link': 'http://github.com/garyvv',
        }
      ],
      activeIndex: '1',
    }
  },
  methods: {
    handleSelect(key, keyPath) {
        console.log(key, keyPath);
    }
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
  text-decoration:none;
}
</style>
