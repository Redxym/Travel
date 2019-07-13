<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: false
      },
      swiperList: [{
        id: '0001',
        imgUrl: require('../../../assets/images/swiper1.jpg')
      }, {
        id: '0002',
        imgUrl: require('../../../assets/images/swiper2.jpg')
      }, {
        id: '0003',
        imgUrl: require('../../../assets/images/swiper3.jpg')
      }
      ]

    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff !important
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 30.47%
    background-color: #eee
    .swiper-img
      width: 100%
</style>
