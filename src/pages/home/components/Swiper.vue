<template>
<div class="wrapper">
  <swiper :options="swiperOptions">
    <swiper-slide v-for="item of swiperList" :key="item.id">
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
    data() {
      return {
        swiperOptions: {
          // 不同版本的小圆点写法不同
          pagination:".swiper-pagination",
          loop: true,
          paginationClickable: true,
          speed:2000,
          autoplay:2000,
        },
        swiperList: [{
            id: '0001',
            imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vcimg/5be2601d1f921f166646b817459a2727.jpeg'
          },{
            id: '0002',
            imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vcimg/280673be5655fc91ce24ba605c62fe07.jpeg'
        }]
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
