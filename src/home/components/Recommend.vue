<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom">
        <img
          class="item-img"
          src="http://img1.qunarzz.com/sight/p0/1508/f7/f7c3be996152011c.img.jpg_200x200_0b707f70.jpg"
        >

        <div class="item-info">
          <p class="item-title">南京总统府</p>
          <p class="item-desc">南京总统府现在已成为记录中国近代史的博物馆。</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeRecommend"
};
</script>

<style lang="stylus" scoped>
.title {
  line-height: 0.8rem;
  margin-top: 0.2rem;
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
}

.item-title {
  line-height: 0.54rem;
  font-size: 0.32rem;
}

.item-desc {
  line-height: 0.4rem;
  color: #ccc;
}

.item-button {
  margin-top: 0.1rem;
  background: #ff9300;
  padding: 0.2rem;
  border-radius: 0.06rem;
  color: #fff;
}
</style>
