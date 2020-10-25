<template>
  <div class="G_game">
    <div>

    </div>
  </div>
</template>

<script>
export default {
    name:'G_game',
    data(){
      return{

      }
    },
    created() {
      this.a1()
    },
    computed: {
      
    },
    methods: {
      a1(){
        // this.axios.get('http://localhost:3000/mv/url?id=5436712')
        // //成功返回
        // .then(res=>{
        //   console.log(res);
        // })
        // //失败返回
        // .catch(error=>{
        //     console.log(error);
        // })
        let api = 'http://localhost:3000/mv/url?id=5436712'
          this.$http({
            url: api,
            method: 'get',
            // 用于用户代理是否应该在跨域请求的情况下向其它域发送cookie，也就是不使用缓存数据；
            withCredentials: true, // 默认为false
            data: {

            }
          }).then(res => {
            console.log(res);
          })
        },
    },
}
</script>

<style>

</style>