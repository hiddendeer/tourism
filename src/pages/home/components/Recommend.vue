<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <img class="item-img" :src="item.imgUrl">

        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button" >查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeRecommend",
  props:{
    list:Array
  },

};
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl';

.title {
  line-height: 0.8rem;
  margin-top: 0.5rem;
  background: #eee;
  text-indent: 0.2rem;
}

.item {
  overflow: hidden;
  display: flex;
  height: 1.9rem;
}

.item-img {
  height: 1.7rem;
  width: 1.7rem;
  padding: 0.1rem;
}

.item-info {
  flex: 1;
  padding: 0.1rem;
  min-width: 0;
}

.item-title {
  overflow: hidden;
  line-height: 0.54rem;
  font-size: 0.28rem;
  ellipsis();
}

.item-desc {
  overflow: hidden;
  line-height: 0.4rem;
  color: #ccc;
  font-size: 0.22rem;
  ellipsis();
}

.item-button {
  margin-top: 0.1rem;
  background: #ff9300;
  padding: 0.07rem;
  border-radius: 0.06rem;
  color: #fff;
}
</style>
