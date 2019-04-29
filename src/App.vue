<template>
  <div id="app">
    <eml-header></eml-header>
    <nav class="nav">
      <div class="seller">
        <router-link to="/seller">seller</router-link>
      </div>
      <div class="goods">
        <router-link to="/goods">goods</router-link>
      </div>
      <div class="ratings">
        <router-link to="/ratings">ratings</router-link>
      </div>
    </nav>
    <router-view></router-view>
  </div>
</template>

<script>
import header from "./components/eml-header"
export default {
  name: 'App',
  components:{
    "eml-header":header
  },
  
}
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
  /*stylus的写法是没有括号和冒号 写了的话没作用*/
  #app
    .nav
      display flex
      &>div
        flex 1
        text-align center
        &.seller
          background yellow
        &.goods
          background red
        &.ratings
          background aqua
      
</style>
