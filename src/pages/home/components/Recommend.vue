<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">{{ item.desc }}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data: function () {
    return {
      recommendList: [{
        id: '1001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1704/a8/a8aa90887648820ba3.img.jpg_200x200_4b2b15a7.jpg',
        title: '红崖谷',
        desc: '浪漫红崖谷首站, 浪漫的红崖谷风景区'
      }, {
        id: '1002',
        imgUrl: 'http://img1.qunarzz.com/sight/p95/201211/03/30f3d57d7f4d4e4a93835fbb.jpg_200x200_f3d8cf9f.jpg',
        title: '石家庄动物园',
        desc: '浪漫石家庄动物园, 浪漫的石家庄动物园景点'
      }, {
        id: '1003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1606/c4/c42772edf8e85f7390.water.jpg_200x200_43eaab86.jpg',
        title: '辛玛王国主题乐园',
        desc: '浪漫辛玛王国主题乐园, 浪漫的辛玛王国主题乐园很好玩'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
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
