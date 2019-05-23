<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      城市
      <span class="iconfont arrow-icon">&#xe64a;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  @import "~styles/variables.stylus";
  .header
    display: flex;
    line-height: 2.8rem;
    background: $bgColor;
    color: #fff;
    .header-left
      width: 2.4rem;
      float: left;
      .back-icon
        text-align: center;
        font-size: 1.2rem;
    .header-input
      flex: 1;
      background: white;
      border-radius: 0.2rem;
      margin-top: 0.4rem;
      line-height: 2rem;
      height: 2rem;
      color: #ccc;
      padding-left: 0.5rem;
    .header-right
      width: 4rem;
      text-align: center;
      .arrow-icon
        font-size: 0.8rem;
        margin-left: -0.3rem;
</style>
