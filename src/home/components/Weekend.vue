<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-wrapper">
          <img class="item-img" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeRecommend",
  data() {
    return {
      recommendList: [
        {
          id: "0001",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1505/f1/ae9d4299b8aaea.jpg_r_640x214_0c555905.jpg",
          title: "南京总统府",
          desc: "南京总统府现在已成为记录中国近代史的博物馆."
        },
        {
          id: "0002",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1505/f1/ae9d4299b8aaea.jpg_r_640x214_0c555905.jpg",
          title: "南京夫子庙",
          desc: "南京夫子庙来南京必去的地方。"
        },
        {
          id: "0003",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1505/f1/ae9d4299b8aaea.jpg_r_640x214_0c555905.jpg",
          title: "南京总统府",
          desc: "南京总统府现在已成为记录中国近代史的博物馆。"
        },
        {
          id: "0004",
          imgUrl:
            "http://img1.qunarzz.com/sight/source/1505/f1/ae9d4299b8aaea.jpg_r_640x214_0c555905.jpg",
          title: "南京总统府",
          desc: "南京总统府现在已成为记录中国近代史的博物馆。"
        }
      ]
    };
  }
};
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl';

.title {
  line-height: 0.8rem;
  margin-top: 0.2rem;
  background: #eee;
  text-indent: 0.2rem;
}

.item-wrapper {
  overflow: hidden;
  height: 0;
  padding-bottom: 33.9%;
}

.item-img {
  width: 100%;
}

.item-info {
  padding: 0.1rem;
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

</style>
