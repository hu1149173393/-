<template>
  <div class="C_son_one">
      <div>
          <ul :key="i" v-for="(v,i) in msg"> 
              <li>
                  {{v.a1}}
              </li>
          </ul>
      </div>
  </div>
</template>

<script>
export default {
    name:'C_son_one',
    data(){
        return {
            msg:[
                {
                    a1:'这是我的网站哦,样式有点难搞哦，交互还没弄。等项目结束好好弄弄'
                }
            ]
        }
    }

}
</script>

<style>
ul li{
    list-style: none;
}
</style>