<template>
  <el-menu
          :default-active="activeIndex"
          class="el-menu-demo"
          mode="horizontal"
          @select="handleSelect"
          background-color="#545c64"
          text-color="#fff"
          active-text-color="#409EFF">
    <el-menu-item v-for="item in menu" :key="item.id" :index="item.id">{{ item.name }}</el-menu-item>
  </el-menu>
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
          'link': 'http://garylv.com',
        },
        {
          'id': '2',
          'name': '博客',
          'class': 'bg-purple-light',
          'icon': 'el-icon-tickets',
          'link': 'http://garylv.com',
        },
        {
          'id': '3',
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
}
</style>
