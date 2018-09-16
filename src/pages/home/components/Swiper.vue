<template>
    <div class="wrapper">
    <swiper :options="swiperOption">
    <!-- slides -->
     <!-- v-for循环轮播图内容 -->
    <swiper-slide v-for="item of swiperList" :key="item.id">
        <img :src="item.imgUrl" :key="item.id"
         class="swiper-img">
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  // es6写法
  // eslint-disable-next-line
  data() {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: '0001',
          imgUrl:
            'http://img1.qunarzz.com/piao/fusion/1809/87/534cf2e0a71fff02.jpg_750x200_5c778719.jpg'
        },
        {
          id: '0002',
          imgUrl:
            'http://img1.qunarzz.com/piao/fusion/1809/28/869966be5963e102.jpg_750x200_f23248ba.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background #ffffff
.wrapper
  overflow hidden
  width 100%
  height 0
  padding-bottom 31.25%
  background #eeeeee
  .swiper-img
    width 100%
</style>
