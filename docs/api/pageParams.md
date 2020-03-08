#### pageParams是表格部分的配置，如下示例：

``` html
<template>
  <VueProTable
    :pageParams="pageParams"
  ></VueProTable>
</template>

<script>
  export default {
    data() {
      return {
        pageParams: {
          total: 0,
          pageNo: 1,
          pageSize: 10,
          showTotal: true
        }
      }
    }
  }
</script>
```


##### pageParams配置

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| current | 当前页码，支持 .sync 修饰符 | Number | 1 |
| total | 数据总数 | Number | 0 |
| page-size | 每页条数 | Number | 10 |
| show-total | 显示总数 | Boolean | false |
| show-elevator | 显示电梯，可以快速切换到某一页 | Boolean | fasle |
| prev-text | 替代图标显示的上一页文字 | String | - |
| next-text | 替代图标显示的下一页文字 | String | - |

