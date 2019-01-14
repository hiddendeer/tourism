<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl">

        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
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
            "http://img1.qunarzz.com/sight/p0/1508/f7/f7c3be996152011c.img.jpg_200x200_0b707f70.jpg",
          title: "南京总统府",
          desc: "南京总统府现在已成为记录中国近代史的博物馆."
        },
        {
          id: "0002",
          imgUrl:
            "http://img1.qunarzz.com/sight/p0/1411/bb/538133c76765880a3d3c802e45015c57.water.jpg_200x200_169b048c.jpg",
          title: "紫清湖生态温泉",
          desc: "钓鱼台小别墅为联体别墅，沿水库大坝临水而建，极目远眺，山水相映，茂林修竹，心 旷神怡。让人真正享受到 “边泡温泉边钓鱼，看看山水发发呆”的境界。"
        },
        {
          id: "0003",
          imgUrl:
            "http://img1.qunarzz.com/sight/p0/1411/b3/1415e635014967c75a3d955ae256a628.water.jpg_200x200_54ee590f.jpg",
          title: "南京汤山一号温泉",
          desc: "由鲜花泉、瓜果泉、咖啡泉等组成的肤之汤，将新鲜的花瓣、瓜果和浓香的精油加入温泉水，有滋润皮肤，美白全身的效果。"
        },
        {
          id: "0004",
          imgUrl:
            "http://img1.qunarzz.com/sight/p0/1504/15/1530936526074f62.water.jpg_200x200_fb55ee43.jpg",
          title: "六朝博物馆",
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
