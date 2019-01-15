<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <swiper-slide v-for="item of list" :key="item.id">
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
  props:{
    list: Array
  },
  data() {
    return {
      swiperOption: {
        pagination: ".swiper-pagination",//banner的凹槽
        loop: true
      },
      mounted() {
        this.swiper.slideTo(3, 1000, false);
      }
    };
  },
  computed:{
    showSwiper() {
      return this.list.length;
    }
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


