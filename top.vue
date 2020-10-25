<template>
  <div class="top">
    <div class="me" @click="value2 = true" type="primary" ><img :src="image2" class="me" alt=""></div>
    <Drawer title="Basic Drawer" placement="left" :closable="false" v-model="value2">
      <p /><a href="www.baidu.com">点我跳百度</a>
      <p /><a href="https://github.com/">点我跳git</a>
      <p /><a href="https://www.csdn.net/">点我跳csdn</a>
      <p /><a href="https://www.bilibili.com/">点我跳哔哩哔哩</a>
    </Drawer>
    <div class="topall">
      <div :key="i" v-for="(v,i) in msg">
        {{v.a1}}
      </div>
    </div>
    <div class="top-left">
      <router-link :to=" { name: 'A_homepage' } " class="tubiao" ><Poptip trigger="hover" content='首页' placement="left"><Icon size='35' class="tubiao2" type="md-laptop" /></Poptip></router-link>  
      <router-link :to=" { name: 'B_saying' } " class="tubiao" ><Poptip trigger="hover" content='说说' placement="left"><Icon size='35' class="tubiao2" type="ios-chatbubbles" /></Poptip>  </router-link> 
      <router-link :to=" { name: 'C_article' } " class="tubiao"><Poptip trigger="hover" content='文章' placement="left"><Icon size='35' class="tubiao2" type="ios-brush" /></Poptip></router-link> 
      <router-link :to=" { name: 'D_work' } " class="tubiao"><Poptip trigger="hover" content='作品' placement="left"><Icon size='35' class="tubiao2" type="ios-desktop-outline" /></Poptip></router-link> 
      <router-link :to=" { name: 'E_books' } " class="tubiao"><Poptip trigger="hover" content='书籍' placement="left"><Icon size='35' class="tubiao2" type="md-book" /></Poptip></router-link> 
      <router-link :to=" { name: 'F_movies' } " class="tubiao"><Poptip trigger="hover" content='影视' placement="left"><Icon size='35' class="tubiao2" type="ios-film-outline" /></Poptip></router-link> 
      <router-link :to=" { name: 'G_game' } " class="tubiao"><Poptip trigger="hover" content='游戏' placement="left"><Icon size='35' class="tubiao2" type="md-game-controller-b" /></Poptip></router-link> 
      <router-link :to=" { name: 'H_music' } " class="tubiao"><Poptip trigger="hover" content='音乐' placement="left"><Icon size='35' class="tubiao2" type="ios-musical-notes-outline" /></Poptip></router-link> 
      <router-link :to=" { name: 'I_my' } " class="tubiao"><Poptip trigger="hover" content='我的' placement="left"><Icon size='35' class="tubiao2" type="md-person" /></Poptip></router-link> 
      <router-link :to=" { name: 'J_setting' } " class="tubiao"><Poptip trigger="hover" content='设置' placement="left"><Icon size='35' class="tubiao2" type="md-snow" /></Poptip></router-link>   
    </div>
    <div class="top-right">
      <router-view />
    </div>

  </div>
</template>

<script>
import $ from 'jquery'
export default {
    name: 'Top',
    data () {
      return {
        msg:[
          {
            a1: '首页',
          },
          {
            a1: '说说',
          },
          {
            a1: '文章',
          },
          {
            a1: '作品',
          },
          {
            a1: '书籍',
          },
          {
            a1: '影视',
          },
          {
            a1: '游戏',
          },
          {
            a1: '音乐',
          },
          {
            a1: '自我',
          },
        ],
        msg2: '设置',
        msg3: false,
        value2: false,
        image2: require('../../assets/me.png'),
    }
  },
  methods:{
    
  }
}
</script>

<style>
.top{
  width: 100%;
  height: 100%;
}
.me{
    width: 50px;
    height: 50px;
    border-radius: 50%;
    position: absolute;
    top: 0;
    left: 11px;
}
.topall{
  width: 95%;
  height: 50px;
  line-height: 50px;
  margin-left: 5%;
  display: flex;
  justify-content: space-around;
}
.top-left{
  width: 8%;
  height: 100%;

}
.tubiao2{
  padding: 5px 5px 5px 30px;
  margin: 5px 5px 5px 0;
  border-top-right-radius:25px;
  border-bottom-right-radius:25px;
    /* border: 1px solid orange; */
}
.top-right{
  width: 94%;
  height: 100%;
  position: absolute;
  top: 60px;
  left: 6%;
}
</style>