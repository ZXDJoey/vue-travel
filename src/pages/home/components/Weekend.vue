<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul class="ul">
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
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
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/fa/ca65fde9677de2.jpg_r_640x214_4500e3ff.jpg',
        title: '深圳必游TOP10',
        desc: '来到深圳，你需要来这里签到'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1602/88/bf120edeaea383.jpg_r_640x214_f8591f7b.jpg',
        title: '欢乐长隆',
        desc: '世界欢乐汇聚长隆'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1507/d9/2ddc7652fdba16.jpg_r_640x214_5e62f1a3.jpg',
        title: '当地人游深圳',
        desc: '当地人带你发现不一样的深圳'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .title
    margin-top: .1rem
    line-height: .8rem
    text-indent: .2rem
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
