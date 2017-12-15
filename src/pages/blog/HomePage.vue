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
      <h1>--- GitHub ---</h1>
      <el-row class="item-list">
        <el-col v-for="card in cards" :key="card.id" :offset="card.id" class="item-list-card">
          <el-tooltip class="item" effect="dark" content="打开项目地址" placement="top">
            <a :href="card.link" target="_blank">
              <el-card :body-style="{ padding: '0px', height: '300px', background: card.color, color: '#fff', paddingTop: '10px'}" >
                <el-tag type="success" class="card-tag">{{ card.name }}</el-tag>
                <div style="padding: 10px;text-align: left">
                  <span v-html="card.content"></span>
                </div>
              </el-card>
            </a>
          </el-tooltip>
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
          'name': 'web-creator',
          'color': '#EC5f67',
          'link': 'https://github.com/garyvv/web-creator',
          'content': '富文本框内容快速生成网页，图片本地化<br />' +
                      '1、富文本框粘贴网页内容，保存自动生成HTML网页，抓取图片进行下载本地化操作；<br />' +
                      '2、支持阿里云OSS上传服务<br />' +
                      '3、可自定义HTML的title、meta，支持SEO优化'
        },
        {
          'id': 2,
          'name': 'wechat-auth',
          'color': '#333',
          'link': 'https://github.com/garyvv/wechat-auth',
          'content': '微信前后端分离登录授权、高拓展性<br />' +
                      '1、基于PHP laravel 框架开发，使用了easyWeChat库<br />' +
                      '2、授权、解析服务端进行处理，多终端统一API处理，开发简单<br />' +
                      '3、公众号配置化自动回复'
        },
        {
          'id': 3,
          'name': 'opencart',
          'color': '#333',
          'link': 'https://github.com/opencart/opencart',
          'content': 'PHP 国外开源商城（业务开发学习推荐）<br />' +
                      '1、成熟的电商系统，阅读源码，有助于提升业务开发能力<br />' +
                      '2、数据库设计，关联数据库设计，规范化的设计和优秀的数据库结构，值得研究学习<br />' +
                      '3、PHPer提升业务开发值得一阅'
        },
        {
          'id': 4,
          'name': 'TODO',
          'color': '#333',
          'link': '/',
          'content': 'To Be Continue'
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
  width: 1024px;
  margin: 0 auto;
  text-align: center;
  border: 1px solid #E4E7ED;
  border-radius: 5px;
  background-color: #909399;
}
.item-list-card {
  width: 25%;
  margin: 20px 4.16%;
  cursor: pointer;
}
.item-list-card :hover {
  opacity: .8;
}
.card-tag {
  color: #fff;
  border-color: rgba(255, 255, 255, .5);
  background-color: rgba(255, 255, 255, .2);
  font-size: 20px;
}
</style>
