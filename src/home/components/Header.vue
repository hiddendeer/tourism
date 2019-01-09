<template>
  <div class="header">
    <div class="header-left">返回</div>
    <div class="header-input">输入城市/景点/游玩主题</div>
    <div class="header-right">城市</div>
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
  color: #fff;
}

.header-left {
  width: 0.64rem;
  float: left;
}

.header-input {
  flex: 1;
  height: 0.64rem;
  line-height: 0.64rem;
  margin-top: 0.12rem;
  margin-left: 0.2rem;
  background: #fff;
  border-radius: 0.1rem;
  color: #ccc;
}

.header-right {
  width: 1.24rem;
  float: right;
  text-align: center;
}
</style>


