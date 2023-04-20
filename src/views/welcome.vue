<template>
   <div class="back">
    <p class="title">欢迎来到陈星旭专场</p>
   </div>
</template>
<script>
export default {
   name: '',
   data() {
       return {}
   },
}
</script>
<style lang='less' scoped>
@import '../common/style/mixin';
.back{
    width: 100%;
    height: 100%;
    background: @primary;
    display: flex;
    justify-content: center;
    align-items: center;
    .title{
        font-size: 20px;
        color: #fff;
        font-weight: bold;
    }
}
</style>
