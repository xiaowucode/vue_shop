<template>
  <div class="tab-bar-item" @click="itemClick">
    <div v-if="!isActived"><slot name="icon-img"></slot></div>
    <div v-else><slot name="icon-img-active"></slot></div>
    <div :style="activedStyle"><slot name="icon-text"></slot></div>
  </div>
</template>
<script>
export default {
  name: "tabBarItem",
  props: {
    path: String,
    activedColor: {
      type: String,
      default: "red",
    },
  },
  data() {
    return {};
  },
  computed: {
    isActived() {
      return !this.$route.path.indexOf(this.path);
    },
    activedStyle() {
      return this.isActived ? { color: this.activedColor } : {};
    },
  },
  methods: {
    itemClick() {
      if (this.$route.path === this.path) return;
      this.$router.replace(this.path);
    },
  },
};
</script>
<style scoped>
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
}
.tab-bar-item img {
  width: 24px;
  height: 24px;
  margin-top: 3px;
  /* 消除图片下方的默认宽度 */
  vertical-align: middle;
  margin-bottom: 2px;
}
</style>