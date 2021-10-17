<template>
  <div>
    <nav-bar class="home">
      <div slot="center">购物街</div>
    </nav-bar>
    <home-swiper :banners="banners"></home-swiper>
  </div>
</template>
<script>
import NavBar from "components/common/navbar/NavBar.vue";
import HomeSwiper from "./childcomps/HomeSwiper.vue";

import { getHomeMultidata } from "network/home.js";

export default {
  name: "home",
  data() {
    return {
      banners: [],
      recommends: [],
    };
  },
  created() {
    getHomeMultidata().then((res) => {
      // console.log(res);
      this.banners = res.data.banner.list;
      this.recommends = res.data.recommend.list;
    });
  },
  components: {
    NavBar,
    HomeSwiper,
  },
};
</script>
<style scoped>
.home {
  background-color: var(--color-tint);
  color: #fff;
}
</style>