<template>
  <div>
<<<<<<< HEAD
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
=======
    <home-header :city="city"></home-header>
    <home-swiper :list="swiperList"></home-swiper>
    <home-icons :list="iconList"></home-icons>
    <home-recommend :list="recommendList"></home-recommend>
    <home-weekend :list="weekendList"></home-weekend>
>>>>>>> index-recommend
  </div>
</template>

<script>
import HomeHeader from './component/Header'
import HomeSwiper from './component/Swiper'
import HomeIcons from './component/Icons'
<<<<<<< HEAD
=======
import HomeRecommend from './component/Recommend'
import HomeWeekend from './component/Weekend'
import axios from 'axios'
>>>>>>> index-recommend

export default {
  name: 'Home',
  components: {
    HomeHeader: HomeHeader,
    HomeSwiper,
<<<<<<< HEAD
    HomeIcons
=======
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  data () {
    return {
      city: '',
      swiperList: [],
      iconList: [],
      recommendList: [],
      weekendList: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.city = data.city
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.recommendList = data.recommendList
        this.weekendList = data.weekendList
      }
    }
  },
  mounted () {
    this.getHomeInfo()
>>>>>>> index-recommend
  }
}
</script>

<style scoped>

</style>
