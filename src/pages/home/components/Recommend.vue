<template>
  <div>
    <div class="title">热销推荐</div>
    <ul class="ul">
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
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1507/64/34362835b4a219af8b36803d31a6380f.water.jpg_200x200_bc5c0452.jpg',
        title: '深圳小梅沙海洋世界',
        desc: '帅的人都去过了，你还等什么～'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201405/30/a9edfcb4fe0e119da480d30d22ade127.jpg_200x200_6af441cf.jpg',
        title: '地王大厦',
        desc: '南望香港，北瞰深圳'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201403/11/c69b992ac22fcf227a04a89bbe597be6.jpg_200x200_9ae54fbd.jpg',
        title: '东门',
        desc: '这里最近很火，好多人都在点评它呢！'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .1rem
    line-height: .8rem
    text-indent: .2rem
  .ul
    padding: 0 0 0 .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem .1rem .1rem 0
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
