<template>
  <div>
    <div>
      <home-header :city="city"></home-header>
      <home-swiper :list="swiperList"></home-swiper>
      <home-icons :list="iconsList"></home-icons>
      <home-recommend :list="recommendList"></home-recommend>
      <home-weekend></home-weekend>
    </div>
  </div>
</template>

<script>
import HomeHeader from "./components/Header";
import HomeSwiper from "./components/Swiper";
import HomeIcons from "./components/Icons";
import HomeRecommend from "./components/Recommend";
import HomeWeekend from "./components/Weekend";
import axios from "axios";

export default {
  name: "Home",
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  data() {
    return {
      city: "南京",
      swiperList: [],
      recommendList: [],
      iconsList: []
    };
  },
  methods: {
    getHomeInfo() {
      axios.get("/api/index.json").then(this.getHomeInfoSucc);
    },
    getHomeInfoSucc(res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data;
        this.swiperList = data.swiperList;
        this.recommendList = data.recommendList;
        this.iconsList = data.iconsList;
      }
    }
  },
  mounted() {
    this.getHomeInfo();
  }
};
</script>

<style>
</style>


