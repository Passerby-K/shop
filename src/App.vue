<template>
  <div id="app">
    <!-- <router-view/> -->
    <headd></headd>
    <div class="content">
        <div class="nav">
            <!-- <a v-link="{path:'/goods'}">商品</a>     -->
            <router-link to="/goods">商品</router-link>
        </div>
        <div class="nav">
            <!-- <a v-link="{path:'/ratings'}">评论</a>   -->
            <router-link to="/ratings">评论</router-link>

        </div>
        <div class="nav">
           <!-- <a v-link="{path:'/seller'}">商家</a>  -->
            <router-link to="/seller">商家</router-link>

        </div>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
import Headd from "./components/head/head"
export default {
  name: 'App',
  components:{
    Headd
  }
}
</script>

<style  lang="stylus" scoped>
.content
    display flex
    width 100%
    line-height 40px
    .nav  
        flex 1
        text-align center
        a
            display block
            font-size 18px
            color black
            &.active
                color red
        
        

</style>
