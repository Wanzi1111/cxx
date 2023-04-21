<template>
  <div class="cxx-info">
    <van-divider class="title">简介</van-divider>
    <div class="info"></div>
  </div>
</template>
<script>
// import { reactive, toRefs } from "vue";
// import { useRouter } from 'vue-router'

export default {
  name: "CxxInfo",
  //   setup() {
  //     const router = useRouter();
  //     const state = reactive({
  //       defaultOptions: {
  //         animationData: Car,
  //         loop: true,
  //         autoplay: true,
  //       },
  //     });
  //     const goTo = () => {
  //       router.push({ path: "/home" });
  //     };
  //     return {
  //       ...toRefs(state),
  //       goTo,
  //     };
  //   },
};
</script>
<style lang='less' scoped>
@import "../common/style/mixin";
.cxx-info {
  background: url("../assets/imges/infoBg.png") no-repeat;
  background-size: 100% 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  .title {
    font-size: 24px;
    // padding: 0 10px;
    font-family: DFPOP;
    margin: 30px auto 20px;
    color: #666;
    border-color: #1baeae;
    font-size: 20px;
    font-weight: 500;
    height: 100px;
    line-height: 100px;
    width: 80%;
  }
}
</style>
