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
  data: function () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          'id': '0001',
          'imgUrl': 'http://img1.qunarzz.com/piao/fusion/1804/15/9250dbc86a456302.jpg_750x200_b423f532.jpg'
        }, {
          'id': '0002',
          'imgUrl': 'http://img1.qunarzz.com/piao/fusion/1805/18/503cb712adf3d502.jpg_750x200_914f9ff7.jpg'
        }, {
          'id': '0003',
          'imgUrl': 'http://img1.qunarzz.com/piao/fusion/1708/f1/ee65a13642c95c02.jpg_750x200_3440fec0.jpg'
        }, {
          'id': '0004',
          'imgUrl': 'http://img1.qunarzz.com/piao/fusion/1804/dd/269c3dafd51a2502.jpg_750x200_4fb86e3e.jpg'
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 26.75%
    background: #eee
    .swiper-img
      width: 100%
</style>
