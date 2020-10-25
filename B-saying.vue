<template>
  <div class="B_saying">
      <div class="b1">
          <ul :key='i' v-for="(v,i) in msg" class="b2">
              <li>{{v.time}}</li>
              <li>{{v.say}}</li>
          </ul>
      </div>
  </div>
</template>

<script>
export default {
    name:'B_saying',
    data(){
        return {
            msg:[
                {
                    time: '2019-08-01',
                    say: '要开始了，感觉还不错'
                },
                {
                    time:'2020-05-01',
                    say: '要开始了，感觉还不错'
                },
                {
                    time:'2019-12-01',
                    say: '要开始了，感觉还不错'
                },
                {
                    time:'2019-11-01',
                    say: '要开始了，感觉还不错'
                },
                {
                    time:'2019-09-01',
                    say: '要开始了，感觉还不错'
                },
                {
                    time:'2019-08-01',
                    say: '要开始了，感觉还不错'
                },
                {
                    time: '2019-07-01',
                    say: '要开始了，感觉还不错'
                },
                {
                    time: '2019-06-01',
                    say: '要开始了，感觉还不错'
                },
            ]
        }
    }
}
</script>

<style>
ul li {
    list-style: none;
}
.b2{
    width: 500px;
    height: 70px;
    line-height: 40px;
    border: 1px solid #e8eaec;
    margin: 20px 0 20px 50px;
    background-color: #f8f8f9;
    box-shadow: f8f8f9;
}
</style>

