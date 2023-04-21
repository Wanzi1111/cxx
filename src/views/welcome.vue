<template>
  <div class="back">
    <img class="logo" src="../assets/imges/logo.png" alt="" />
    <h1 class="title">Welcome to CXX special show</h1>
    <div class="car-logo">
      <lottie :options="defaultOptions" @click="goTo" />
      <p>点击小车开启旅程</p>
    </div>
  </div>
</template>
<script>
import { reactive, toRefs } from "vue";
import Car from "../assets/lottie/car-loading5-data.json";
import { useRouter } from 'vue-router'

export default {
  name: "",
  setup() {
    const router = useRouter();
    const state = reactive({
      defaultOptions: {
        animationData: Car,
        loop: true,
        autoplay: true,
      },
    });
    const goTo = () => {
      router.push({ path: "/CxxInfo" });
    };
    return {
      ...toRefs(state),
      goTo,
    };
  },
};
</script>
<style lang='less' scoped>
@import "../common/style/mixin";
.back {
  background: @primary;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  .logo {
    width: 120px;
    height: 120px;
    display: block;
    margin: 0px auto 20px;
  }
  .title {
    font-size: 20px;
    color: #fff;
    font-weight: bold;
    font-family: Sugar;
  }
  .car-logo {
    height: 80px;
    display: block;
    p {
      width: 100%;
      color: #fff;
      display: inline-block;
      font-family: DFPOP;
      font-weight: bold;
      text-align: center;
    }
  }
}
</style>
