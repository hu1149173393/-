<template>
  <div class="C_article">
      <div>
        <Menu mode="horizontal" :theme="theme1" active-name="1">
            <MenuItem name="1" to='C_son_one'>
                <Icon type="ios-paper" />
                前端学习
            </MenuItem>
            <MenuItem name="2" to='C_son_two'>
                <Icon type="ios-paper" />
                网络请求
            </MenuItem>
            <MenuItem name="3" to='C_son_three'>
                <Icon type="ios-paper" />
                vue学习
            </MenuItem>
            <MenuItem name="4" to='C_son_fore'>
                <Icon type="ios-paper" />
                react学习
            </MenuItem>
        </Menu>
      </div>
      <router-view />
  </div>
</template>

<script>
export default {
    name:'C_article',
    data () {
        return {
            theme1: 'light'
        }
    }
}
</script>

<style>

</style>