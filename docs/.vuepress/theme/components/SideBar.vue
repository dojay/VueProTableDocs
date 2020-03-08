<template>
  <div class="d-sidebar">
    <div class="big-title">开发指南</div>
    <ul>
      <li :class="{active: active === 'quickstart'}" @click="handlerClick('quickstart')">快速上手</li>
      <li :class="{active: active === 'log'}" @click="handlerClick('log')">更新日志</li>
    </ul>

    <div class="big-title">教程</div>
    <div v-for="item in siderData" :key="item.title">
      <!-- <div class="middle-title">{{ item.title }}</div> -->
      <ul>
        <li :class="{active: active === list.url}" v-for="list in item.list" @click="handlerClick(list.url)">
          {{list.title}}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        siderData: [
          // {
          //   title: '布局',
          //   list: [
          //     { title: 'Grid 宫格', url: 'grid' },
          //     { title: 'List 列表', url: 'list' },
          //     { title: 'Panel 面板', url: 'panel' }
          //   ]
          // }
          {
            list: [
              { title: 'API', url: 'api' },
              { title: 'searchConfig 搜索配置', url: 'searchConfig' },
              { title: 'tableParams 表格配置', url: 'tableParams' },
              { title: 'pageParams 分页配置', url: 'pageParams' }
            ]
          }
        ],
        active: 'quickstart'
      }
    },
    mounted() {
      const pathname = location.pathname;

      if (pathname) {
        this.active = pathname.substring(12).split('.')[0];
      }
    },
    methods: {
      handlerClick (link) {
        this.$router.push(link + '.html')
        this.active = link;
      }
    }
  }
</script>

<style lang="stylus">
  .d-sidebar
    position absolute
    top 64px
    left 0
    width 200px
    height calc(100vh - 64px)
    border-right 1px solid #ddd
    overflow scroll
    padding-bottom 40px
    box-sizing border-box

    .big-title
      font-size 16px
      height 48px
      line-height 48px
      padding-left 15px
      font-weight bold
      color #333333

    .middle-title
      font-size 14px
      height 40px
      line-height 40px
      padding-left 20px
      color #999

    ul
      list-style none
      padding-left 0
      line-height 1
      margin 0
      li
        height 44px
        font-size 12px
        line-height 44px
        cursor pointer
        padding-left 34px
        &:hover
          background #f3f3f3
        &.active
          color #36CFC9
          border-right 2px solid #36CFC9
</style>