<template>
  <div class="d-home">
    <h1>{{data.title}}</h1>
    <div class="desc">{{data.desc}}</div>
    <div class="quickstart">
      <router-link :to="data.link">开始探索 →</router-link>
    </div>
  </div>
</template>

<script>
  export default {
    name: '',
    data() {
      return {}
    },
    computed: {
      data() {
        return this.$page.frontmatter
      }
    }
  }
</script>

<style lang="stylus">
  .d-home
    display flex
    align-items center
    flex-direction column
    justify-content center
    h1
      padding 120px 0 20px
    .desc
      font-size 14px
      color #666
    .quickstart
      width 140px
      height 44px
      border-radius 22px
      background #46bd87
      line-height 44px
      text-align center
      margin-top 100px

      a
        text-decoration none
        font-size 14px
        color #ffffff
</style>