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
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1802/40/40b2075640718d7a3.img.png_256x160_778f7d0b.png',
        title: '天门山国家森林公园',
        desc: '穿越云霄的旅行'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/sight/p0/1612/14/14bef79602a7780a3.water.jpg_256x160_3424b8ae.jpg',
        title: ' 张家界',
        desc: '湘鄂渝黔革命根据地的发源地和中心区域'
      }, {
        id: '0003',
        imgUrl: 'https://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/646e244028cb286586e2cb0aa9dd63dc.jpg',
        title: '丽江',
        desc: '一路向南，丽江的故事等你倾听'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-index: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
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
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
