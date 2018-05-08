<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" />
        </div>
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">{{ item.desc }}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data: function () {
    return {
      recommendList: [{
        id: '1001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/d1/3070ad726f861b.jpg_r_640x214_39709b85.jpg',
        title: '石家庄必游TOP5',
        desc: '旅游资源丰富，名胜古迹众多'
      }, {
        id: '1002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1507/82/06e79c5f8d6e7.jpg_r_640x214_5e63707e.jpg',
        title: '当地人玩什么',
        desc: '石家庄人民周末好玩法'
      }, {
        id: '1003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1703/e1/93571b553ed1aa.jpg_r_640x214_a7c8c3f6.jpg',
        title: '风景胜地',
        desc: '快来一睹河北风光'
      }, {
        id: '1004',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1703/76/21c150b21ba32b.jpg_r_640x214_00bcca2c.jpg',
        title: '欢乐亲子游',
        desc: '享受亲子时光，带宝贝欢乐游玩'
      }, {
        id: '1005',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1703/c8/c21ee1e6556561.jpg_r_640x214_e47f78ad.jpg',
        title: '张家口必游TOP5',
        desc: '一定要去哦！'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 37.09%
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
