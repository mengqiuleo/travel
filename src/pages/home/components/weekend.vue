<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom"
      v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
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
  name: 'HomeWeekend',
  data() {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vs_tts/0a0cef49-07cd-4835-ba2b-763026f116e0.jpg_r_390x260x95_19e75b6a.jpg',
        title: '大连圣亚海洋世界',
        desc: '晚清时期的中国金融中心'
      },{
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vs_tts/0a0cef49-07cd-4835-ba2b-763026f116e0.jpg_r_390x260x95_19e75b6a.jpg',
        title: '大连圣亚海洋世界',
        desc: '晚清时期的中国金融中心'
      },{
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vs_tts/0a0cef49-07cd-4835-ba2b-763026f116e0.jpg_r_390x260x95_19e75b6a.jpg',
        title: '大连圣亚海洋世界',
        desc: '晚清时期的中国金融中心'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~style/mixins'

  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 33.9%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()

</style>

/*
文本首行缩进
text-indent
 */
