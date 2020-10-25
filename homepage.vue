<template>
  <div class="homepage">
      
      <div @mouseleave="a2" :class=" iscolo == false ? 'homepage-one' : 'homepage_one' ">
        <p>
            <span>{{ msg_1 }}</span>
            <router-link :to=" { name: 'Top' } " @mouseenter.native="a1" ><u>{{ msg_2 }}</u></router-link>
            <span>{{ msg_3 }}</span>
        </p>
        <p>
            <span>{{ msg_4 }}</span>
            <router-link :to=" { name: 'Top' } " @mouseenter.native="a1" ><u>{{ msg_5 }}</u></router-link>
            <span>{{ msg_6 }}</span>
            <router-link :to=" { name: 'Top' } " @mouseenter.native="a1" ><u>{{ msg_7 }}</u></router-link>
            <span>{{ msg_8 }}</span>
        </p>
        <p>
            <span>{{ msg_9 }}</span>
            <router-link :to=" { name: 'Top' } " @mouseenter.native="a1" ><u>{{ msg_10 }}</u></router-link>
            <span>{{ msg_11 }}</span>
        </p>
      </div>
      <div class="homepage_background">
          <img v-show="isshow1" :src="image1" alt="" class="homepage_background_img">
      </div>
  </div>
</template>

<script>
export default {
    name:'homepage',
    data () {
        return {
            msg_1: '想走的',
            msg_2: '路',
            msg_3: '不好走，想做人不好做，都说是身不由己，不是废话么。己不由心 身又岂能由己！',
            msg_4: '判断一个人不应该听他说',
            msg_5: '说',
            msg_6: '过什么，而应该看他都',
            msg_7: '做',
            msg_8: '过什么。一个成熟的男人应该,知道自己当下最需要什么,又该放弃什么,要做的这点需要一定的素质，隐忍、坚毅、甚至是凶狠。',
            msg_9: '过去无可挽回',
            msg_10: '未来',
            msg_11: '可以改变!',

            image1: require('../assets/背景new.jpg'),
            isshow1: false,
            iscolo: false,
            
        }
    },
    created(){

    },
    methods: {
        a1(){
           this.isshow1 = true
           this.iscolo = true

        },
        a2(){
            this.isshow1 = false
            this.iscolo = false
        },
    },
    computed: {

    },  


}
</script>

<style>
.homepage{
    width: 100%;
    height: 600px;
    text-align: center;
    line-height: 80px;
    position: relative;
    background-color: white;
}

.homepage-one{
    width: 100%;
    height: 300px;

    position: absolute;
    top: 0;
    bottom: 0;
    margin: auto;
    z-index: 2;
    background-color: white;
    color: orange;
}
.homepage_one{
    width: 100%;
    height: 300px;
    position: absolute;
    top: 0;
    bottom: 0;
    margin: auto;
    z-index: 2;
    background-color: rgba(0, 0, 0, 0.3);
    color: white;
}
.homepage_background{
    width: 100%;
    height: 600px;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 1;
}
.homepage_background_img{
    width: 100%;
    height: 100%;
}
</style>