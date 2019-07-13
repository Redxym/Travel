<template>
  <div class="icons">
<<<<<<< HEAD
    <swiper>
=======
    <swiper :options="swiperOption">
>>>>>>> index-recommend
      <swiper-slide v-for="(page, index) of pages" :key="index">
      <div class="icon" v-for="item of page" :key="item.id">
        <div class="icon-img">
          <img class="icon-img-content" :src="item.imgUrl">
        </div>
        <p class="icon-desc">{{item.desc}}</p>
      </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
<<<<<<< HEAD
  data () {
    return {
      iconList: [{
        id: '0001',
        imgUrl: 'http://s.qunarzz.com/homenode/images/touchheader/group.png',
        desc: '特惠酒店'
      }, {
        id: '0002',
        imgUrl: 'http://s.qunarzz.com/homenode/images/touchheader/bargainflight.png',
        desc: '低价门票'
      }, {
        id: '0003',
        imgUrl: 'http://s.qunarzz.com/homenode/images/touchheader/inn.png',
        desc: '客栈'
      }, {
        id: '0004',
        imgUrl: 'http://s.qunarzz.com/homenode/images/touchheader/haiwai.png',
        desc: '海外酒店'
      }, {
        id: '0005',
        imgUrl: 'http://s.qunarzz.com/homenode/images/touchheader/kezhan.png',
        desc: '民宿'
      }, {
        id: '0006',
        imgUrl: 'http://s.qunarzz.com/homenode/images/touchheader/bus.png',
        desc: '汽车票船票'
      }, {
        id: '0007',
        imgUrl: 'http://s.qunarzz.com/homenode/images/touchheader/tuan.png',
        desc: '旅游团购'
      }, {
        id: '0008',
        imgUrl: 'http://s.qunarzz.com/homenode/images/touchheader/freeTravel.png',
        desc: '自由行'
      }, {
        id: '0009',
        imgUrl: 'http://s.qunarzz.com/homenode/images/touchheader/car.png',
        desc: '专车自驾'
      }, {
        id: '0010',
        imgUrl: 'http://s.qunarzz.com/homenode/images/touchheader/aroundtravel.png',
        desc: '周边短途'
      }, {
        id: '0011',
        imgUrl: 'http://s.qunarzz.com/homenode/images/touchheader/aroundtravel.png',
        desc: '周边短途'
      }]
=======
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        autoplay: false
      }
>>>>>>> index-recommend
    }
  },
  computed: {
    pages () {
      const pages = []
<<<<<<< HEAD
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 10)
=======
      this.list.forEach((item, index) => {
        const page = Math.floor(index / 8)
>>>>>>> index-recommend
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  @import "~styles/mixins.styl"
  .icons >>> .swiper-container
    overflow: hidden
    height: 0
    padding-bottom: 50%
<<<<<<< HEAD
    background: pink
=======
  .icons
    margin-top: .1rem
>>>>>>> index-recommend
    .icon
      position: relative
      overflow: hidden
      float: left
<<<<<<< HEAD
      width: 20%
=======
      width: 25%
>>>>>>> index-recommend
      height: 0
      padding-bottom: 25%
      background: #fff
      .icon-img
        position: absolute
        top: 0
        left: 0
        right: 0
        bottom: .44rem
        .icon-img-content
          display: block
          width: 50%
          margin: 0 auto
          height: 100%
      .icon-desc
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: .44rem
        line-height: .44rem
        text-align: center
        color: $darkTextColor
        ellipsis()
</style>
