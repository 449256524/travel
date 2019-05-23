<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl">
          </div>
          <p class="icon-desc">{{item.name}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      swiperOption: {
        loop: false
      },
      'iconList': [
        {
          id: 1,
          name: '景点门票',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png'
        },
        {
          id: 2,
          name: '一日游',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/f0f00d6dfe038c044dbc9a437f58b0eb.png'
        },
        {
          id: 3,
          name: '必游',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png'
        },
        {
          id: 4,
          name: '溜娃儿',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png'
        },
        {
          id: 5,
          name: '爬长城',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20191/0334cf5430b9b5505fd79e2b8d7e8670.png'
        },
        {
          id: 6,
          name: '故宫',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png'
        },
        {
          id: 7,
          name: '动植物园',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png'
        },
        {
          id: 8,
          name: '限时抢购',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/35d83bb968d80d54926f30cfb92cb6ff.png'
        },
        {
          id: 9,
          name: '欢乐谷',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/338c5b924c5809e8c7b14f60a953c3e2.png'
        }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
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
  @import "~styles/variables.stylus";
  @import "~styles/mixins.styl";
  .icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
  .icon
    position: relative;
    float: left
    width: 25%
    height: 0
    padding-bottom: 25%
    overflow: hidden
    .icon-img
      position: absolute
      height 70%
      top: 0
      left: 0
      right: 0
      bottom: 1rem
      box-sizing: border-box
      padding: 0.1rem
      .icon-img-content
        display: block
        margin:0 auto
        height: 100%
    .icon-desc
      position: absolute
      left: 0
      right: 0
      bottom: 0.8rem
      height: 1rem
      text-align: center
      line-height: 1rem
      color: $darkTextColor
      ellipse()
</style>
