<template>
  <tab-bar>
      <tab-bar-item path='/home'>
        <img slot="icon-img" src="~assets/img/tabbar/home.svg" alt="" />
        <img slot="icon-img-active" src="~assets/img/tabbar/home_active.svg" alt="" />
        <div slot="icon-text">首页</div>
      </tab-bar-item>
      <tab-bar-item path='/category'>
        <img slot="icon-img" src="~assets/img/tabbar/category.svg" alt="" />
        <img slot="icon-img-active" src="~assets/img/tabbar/category_active.svg" alt="" />
        <div slot="icon-text">分类</div>
      </tab-bar-item>
      <tab-bar-item path='/cart'>
        <img slot="icon-img" src="~assets/img/tabbar/shopcart.svg" alt="" />
        <img slot="icon-img-active" src="~assets/img/tabbar/shopcart_active.svg" alt="" />
        <div slot="icon-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item path='/profile'>
        <img slot="icon-img" src="~assets/img/tabbar/profile.svg" alt="" />
        <img slot="icon-img-active" src="~assets/img/tabbar/profile_active.svg" alt="" />
        <div slot="icon-text">我的</div>
      </tab-bar-item>
    </tab-bar>
</template>
<script>
import tabBar from "components/common/tabbar.vue";
import tabBarItem from "components/common/tabbaritem.vue";
export default {
  name: "mainTabBar",
  components: {
    tabBar,
    tabBarItem
  },
}
</script>
<style scoped>

</style>