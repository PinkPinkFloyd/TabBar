<template>
  <div id="app">
    <tab-bar>
       <tab-bar-item path="/home" activeColor="blue">
         <img slot="item-icon" src="./assets/img/tabbar/home.png" alt="">
         <img slot="item-icon-active" src="./assets/img/tabbar/home_active.png" alt="">
         <div slot="item-text">首页</div>
       </tab-bar-item>
       <tab-bar-item path="/category" activeColor="blue">
          <img slot="item-icon" src="./assets/img/tabbar/categories.png" alt="">
          <img slot="item-icon-active" src="./assets/img/tabbar/categories_active.png" alt="">
          <div slot="item-text">分类</div>
       </tab-bar-item>
       <tab-bar-item path="/shopcart" activeColor="blue">
          <img slot="item-icon" src="./assets/img/tabbar/shopcart.png" alt="">
          <img slot="item-icon-active" src="./assets/img/tabbar/shopcart_active.png" alt="">
          <div slot="item-text">购物车</div>
       </tab-bar-item>
       <tab-bar-item path="/profile" activeColor="blue">
          <img slot="item-icon" src="./assets/img/tabbar/profile.png" alt="">
          <img slot="item-icon-active" src="./assets/img/tabbar/profile_active.png" alt="">
          <div slot="item-text">我的</div>
       </tab-bar-item>
    </tab-bar>
    <router-view></router-view>
  </div>
</template>

<script>
import TabBar from "./components/tabbar/TabBar.vue";
import TabBarItem from "./components/tabbar/TabBarItem.vue"
export default {
  name: "App",
  components: {
    TabBar,
    TabBarItem
  }
};
</script>

<style>
@import "./assets/css/base.css";

</style>
