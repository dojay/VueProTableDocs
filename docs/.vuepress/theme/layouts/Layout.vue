<template>
  <div class="theme-container">
    <!-- 导航 -->
    <NavBar />
    <div class="d-page-box">
      <!-- 侧边导航 -->
      <SideBar v-if="!$page.frontmatter.home"></SideBar>
      <!-- 首页 -->
      <Home v-if="$page.frontmatter.home"></Home>
      <!-- 页面 -->
      <Page v-else></Page>
    </div>
  </div>
</template>

<script>
  import NavBar from '@theme/components/NavBar.vue'
  import SideBar from '@theme/components/SideBar.vue'
  import Home from '@theme/components/Home.vue'
  import Page from '@theme/components/Page.vue'

  export default {
    name: '',
    data() {
      return {
        
      }
    },
    components: {
      NavBar,
      SideBar,
      Home,
      Page
    }
  }
</script>

<style lang="stylus" scoped>
  @require '../styles/index.styl'
  .d-page-box{
    width 1024px
    margin 0 auto
    position relative
  }
</style>