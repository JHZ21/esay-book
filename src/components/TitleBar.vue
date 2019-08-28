<template>
  <transition name="slide-down">
    <div class="tittle-wrapper" v-show="ifTitleAndMenuShow">
      <div class="left">
        <span class="iconfont icon-back"></span>
      </div>
      <div class="right">
        <span class="icon-wrapper">
          <i class="iconfont icon-cart"></i>
        </span>
        <span class="icon-wrapper">
          <i class="iconfont icon-person"></i>
        </span>
        <span class="icon-wrapper">
          <i class="iconfont icon-more"></i>
        </span>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  name: "TitleBar",
  props: {
    ifTitleAndMenuShow: {
      type: Boolean,
      default: false
    }
  }
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/global";
.tittle-wrapper {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 101;
  display: flex;
  width: 100%;
  height: px2rem(48);
  background: white;
  box-shadow: 0 px2rem(8) px2rem(8) rgba(0, 0, 0, 0.15);
  .left {
    flex: 0 0 px2rem(60);
    @include center;
  }
  .right {
    display: flex;
    flex: 1;
    justify-content: flex-end;
    .icon-wrapper {
      flex: 0 0 px2rem(40);
      @include center;
    }
  }
}
</style>
