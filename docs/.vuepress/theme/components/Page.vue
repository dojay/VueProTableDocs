<template>
  <div class="d-page">
    <Content class="d-content custom" />
  </div>
</template>

<script>
  export default {
    name: '',
    data() {
      return {
        
      }
    }
  }
</script>

<style lang="stylus">
  .d-page
    position absolute
    top 64px
    left 200px
    height calc(100vh - 64px)
    overflow scroll
    padding-left 40px
    width 800px

    .d-content
      padding-bottom 100px
</style>