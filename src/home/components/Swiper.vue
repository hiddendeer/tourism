<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of SwiperList" :key="item.id">
        <img :src="item.imgUrl" class="swiper-img">
      </swiper-slide>

      <div class="swiper-pagination" slot="pagination"></div>
      <div class="swiper-scrollbar" slot="scrollbar"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: "HomeSwiper",
  data() {
    return {
      swiperOption: {
        pagination: ".swiper-pagination",
        loop: true
      },
      SwiperList: [
        {
          id: "001",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1811/a8/cb43c4ac6c215d02.jpg_750x200_83dee994.jpg"
        },
        {
          id: "002",
          imgUrl:
            "http://img1.qunarzz.com/piao/fusion/1901/8d/23ccea765cb00c02.jpg_750x200_d72d781d.jpg"
        }
      ],
      mounted() {
        this.swiper.slideTo(3, 1000, false);
      }
    };
  }
};
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active {
  background: #fff;
}

.wrapper {
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 26.70%;

  .swiper-img {
    width: 100%;
  }
}
</style>


