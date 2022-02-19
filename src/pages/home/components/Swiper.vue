<template>
<div class="wrapper">
  <swiper :options="swiperOptions" v-if="list.length">
    <swiper-slide v-for="item of list" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl">
    </swiper-slide>

    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</div>
</template>

<script>
// import 'swiper/dist/css/swiper.css'
// import { swiper, swiperSlide } from 'vue-awesome-swiper'

  export default {
    name: 'HomeSwiper',
    props: {
      list: Array
    },
    data() {
      return {
        swiperOptions: {
          // 不同版本的小圆点写法不同
          pagination:".swiper-pagination",
          loop: true,
          paginationClickable: true,
          speed:2000,
          autoplay:2000,
        }
      }
    }
  }
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width 100%
    height: 0
    padding-bottom: 31.25%
    .swiper-img
      width: 100%
</style>
