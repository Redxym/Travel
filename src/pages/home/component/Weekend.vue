<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of weekendList" :key="item.id">
        <div class="item-img-wrapper">
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
    name: 'HomeWeekend',
    data () {
      return {
        weekendList: [{
          id: '0001',
          imgUrl: 'https://tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/42c26df35be02c4f8e691511b392c293.jpg',
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
