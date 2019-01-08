<template>
  <div class="header">
    <div class="header-left">返回</div>
    <div class="header-input">搜索</div>
    <div class="header-right">图标</div>
  </div>
</template>

<script>
export default {
  name: "HomeHeader"
};
</script>

<style lang="stylus" scoped>
.header {
  display: flex;
  line-height: 0.86rem;
  background: #00bcd4;
  color: #fff
}

.header-left {
  width: 0.64rem;
  float: left;
}

.header-input {
  flex: 1;
}

.header-right {
  width: 1.24rem;
  float: right;
}
</style>


