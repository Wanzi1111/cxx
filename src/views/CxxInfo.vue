<template>
  <div class="cxx-info">
    <van-divider class="title">简介</van-divider>
    <div class="info">
      <span
        >陈星旭，1996年3月31日出生于辽宁沈阳，中国内地男演员，中戏14级表演系毕业</span
      >
      <ul class="list">
        <li v-for="(item, index) in infoData" :key="index"><label>{{item.title}}: </label> {{item.value}}</li>
      </ul>
      <div class="btn">
        <van-button color="#1baeae" plain class="next">next</van-button>
      </div>
    </div>
  </div>
</template>
<script>
import { reactive, toRefs } from "vue";
// import { useRouter } from 'vue-router'

export default {
  name: "CxxInfo",
    setup() {
      // const router = useRouter();
      const state = reactive({
        infoData: [{
          title: '陈星旭',
          value: '1996/03/31'
        },{
          title: '身高',
          value: '186cm'
        },{
          title: '星座',
          value: '白羊座'
        },{
          title: '毕业院校',
          value: '毕业于北京蓝天幼儿园、北京海淀区外国语学院、北舞附中、中央戏剧学院（2014中戏表演专业第一）'
        },{
          title: '常见昵称',
          value: '九，亮亮，小陈，小陈同学，星旭等'
        },{
          title: '粉丝名',
          value: '小星星'
        },{
          title: '应援色',
          value: '柿子橙/星空蓝'
        },]
      });
      // const goNext = () => {
      //   router.push({ path: "/home" });
      // };
      return {
        ...toRefs(state),
        // goNext,
      };
    },
};
</script>
<style lang='less' scoped>
@import "../common/style/mixin";
.cxx-info {
  height: 100%;
  background: url("../assets/imges/infoBg.png") no-repeat;
  background-size: 100% 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 0 40px;
  position: relative;
  .title {
    font-family: DFPOP;
    color: #666;
    border-color: #1baeae;
    font-size: 28px;
    font-weight: 500;
    height: 100px;
    line-height: 100px;
    width: 100%;
  }
  .info {
    width: 100%;
    font-size: 16px;
    span {
      display: inline-block;
      text-indent: 2em;
    }
    .list {
      margin-top: 60px;
      line-height: 40px;
      label {
        color: #1baeae;
        font-weight: bold;
      }
    }
    .btn {
      .cl();
      bottom: 50px;
      .next {
        display: inline-block;
        width: 55px;
        height: 30px;
        .borderRadius(10px);
        border: 1px solid #66e0ff;
      }
    }
  }
}
</style>
