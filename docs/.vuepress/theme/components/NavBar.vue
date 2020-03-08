<template>
  <div class="d-navbar">
    <div class="logo">
      <span class="logo-txt">VueProTable</span>
    </div>
    <div class="menu-box">
      <div 
        class="menu-item"
        v-for="(item, index) in navData"
        :key="index"
      >
        <router-link :to="item.link">{{item.text}}</router-link>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: '',
    data() {
      return {
      }
    },
    computed: {
      navData() {
        return this.$site.themeConfig.nav
      }
    }
  }
</script>

<style lang="stylus">
  .d-navbar
    position fixed
    height 64px
    top 0
    left 0
    right 0
    z-index 99
    padding 0 60px
    box-shadow 0 0 4px #eee
    display flex
    flex-direction row
    align-items center
    justify-content space-between
    .logo
      .logo-txt
        font-size 24px
        font-weight 500
        line-height 64px
    .menu-box
      .menu-item
        position relative
        margin-left 40px
        display inline-block
        height 64px
        a
          color #4d5164
          font-size 14px
          line-height 64px
          letter-spacing 0px
          text-decoration none
</style>