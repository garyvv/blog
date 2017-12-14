<template>
  <el-container>
    <el-header><Header /></el-header>

    <el-main>
      <!-- 走马灯 -->
      <el-carousel :interval="4000" type="card" height="260px"  style="background-color: #545c63">
        <el-carousel-item v-for="item in banners" :key="item.id">
          <a :href="item.link"><img :src="item.image" class="card-img" /></a>
        </el-carousel-item>
      </el-carousel>

      <!-- GitHub 推荐 -->
      <h1>GitHub</h1>
      <el-row class="item-list">
        <el-col v-for="card in cards" :key="card.id" :offset="card.id" class="item-list-card">
          <el-card :body-style="{ padding: '0px', height: '300px', background: card.color, color: '#fff', paddingTop: '10px'}" >
            <el-tag type="success">{{ card.name }}</el-tag>
            <div style="padding: 10px;text-align: left">
              <span>{{ card.content }}</span>
            </div>
          </el-card>
        </el-col>
      </el-row>

    </el-main>

    <el-footer><Footer /></el-footer>
  </el-container>
</template>

<script>
import Header from '@/components/BlogHeader'
import Footer from '@/components/BlogFooter'
import ElFooter from "../../../node_modules/element-ui/packages/footer/src/main";
import ElCol from "element-ui/packages/col/src/col";
export default {
  name: 'HomePage',
  data () {
    return {
      //      card
      banners: [
        {
          'id': 1,
          'image': 'http://toy.garylv.com/image/cache/catalog/Banner/IMG_5545-1140x380.JPG',
          'link': 'http://toy.garylv.com/'
        },
        {
          'id': 2,
          'image': 'http://toy.garylv.com/image/cache/catalog/Banner/IMG_5548-1140x380.JPG',
          'link': 'http://toy.garylv.com/'
        },
        {
          'id': 3,
          'image': 'http://toy.garylv.com/image/cache/catalog/Banner/bianxingjingang-1140x380.jpg',
          'link': 'http://toy.garylv.com/'
        },
      ],
      cards: [
        {
          'id': 1,
          'name': 'web-creator 1',
          'color': '#333',
          'content': 'laravel 的 一些laravel 的 一些laravel 的 一些laravel 的 一些laravel 的 一些laravel 的 一些laravel 的 一些'
        },
        {
          'id': 2,
          'name': 'wechat-auth 2',
          'color': '#333',
          'content': 'jdsalfjdslkafjlasdjf slkdajflsdjafj http://toy.garylv.com/'
        },
        {
          'id': 3,
          'name': 'oc-api 3',
          'color': '#333',
          'content': 'jdsalfjdslkafjlasdjf slkdajflsdjafj http://toy.garylv.com/'
        },
        {
          'id': 4,
          'name': 'web-creator 4',
          'color': '#333',
          'content': 'laravel 的 一些laravel 的 一些laravel 的 一些laravel 的 一些laravel 的 一些laravel 的 一些laravel 的 一些'
        },
        {
          'id': 5,
          'name': 'wechat-auth 5',
          'color': '#333',
          'content': 'jdsalfjdslkafjlasdjf slkdajflsdjafj http://toy.garylv.com/'
        },
        {
          'id': 6,
          'name': 'oc-api 6',
          'color': '#333',
          'content': 'jdsalfjdslkafjlasdjf slkdajflsdjafj http://toy.garylv.com/'
        },
      ],
    }
  },
  components: {
    ElCol,
    ElFooter,
    Header,
    Footer
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
.card-img {
  height: 300px;
  width: auto;
}
.item-list {
  width: 75%;
  margin: 0 auto;
  text-align: center;
  border: 1px solid #545c63;
  border-radius: 5px;
}
.item-list-card {
  width: 25%;
  margin: 20px 4.16%;
}
</style>
