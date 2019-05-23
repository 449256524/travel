<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList"  :key="item.id">
        <img class="swip-img" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
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
        autoplay: 3000,
        loop: true
      },
      swiperList: [
        {
          id: 1,
          imgUrl: 'https://pic5.40017.cn/03/000/a8/97/rBANB1zb3NKAIcyiAADgNXpg8ZU886.jpg'
        },
        {
          id: 2,
          imgUrl: 'https://pic5.40017.cn/03/000/00/38/rBANB1zeeuqAUS1PAADvE6D5kJI344.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: white !important
  .wrapper
    overflow:hidden
    width: 100%
    height: 0
    padding-bottom: 25.23%
    background: #ccc
    .swip-img
      width: 100%
</style>
