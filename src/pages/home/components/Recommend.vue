<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom"
      v-for="item of recommendList" :key="item.id">
          <img class="item-img" :src="item.imgUrl" alt="">

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
  name: 'HomeRecommend',
  data() {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vs_tts/0a0cef49-07cd-4835-ba2b-763026f116e0.jpg_r_390x260x95_19e75b6a.jpg',
        title: '大连圣亚海洋世界',
        desc: '晚清时期的中国金融中心'
      },{
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1505/f0/f04df22f36d4dc25.water.jpg_710x360_48a463e0.jpg',
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
  .item
    display: flex
    height: 1.9rem
    overflow: hidden
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .item-button
        padding: 0  .2rem
        line-height: .44rem
        background: #ff9300
        border-radius: .06rem
        margin-top: .16rem
        color: #fff
</style>

/*
文本首行缩进
text-indent
 */
