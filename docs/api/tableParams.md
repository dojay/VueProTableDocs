#### tableParams是表格部分的配置，如下示例：

``` html
<template>
  <VueProTable
    :tableParams="tableParams"
  ></VueProTable>
</template>

<script>
  export default {
    data() {
      return {
        tableParams: {
          columns: [
            {title: '订单号', key: 'orderNo', align: 'center', minWidth: 100},
            {title: '操作', slot: 'orderNo', align: 'center', minWidth: 200}
          ],
          data: [],
          border: true,
          stripe: true,
          height: 300
        }
      }
    }
  }
</script>
```


##### tableParams配置

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| columns | 表格列的配置描述 | Array | [] |
| stripe | 是否显示间隔斑马纹 | Boolean | false |
| border | 是否显示纵向边框 | Boolean | false |
| height | 表格高度，单位 px，设置后，如果表格内容大于此值，会固定表头 | Number or String | - |
| max-height | 表格最大高度，单位 px，设置后，如果表格内容大于此值，会固定表头 | Number or String | - |
| loading | 表格是否加载中 | Boolean | false |
| disabled-hover | 禁用鼠标悬停时的高亮 | Boolean | false |
| no-data-text | 数据为空时显示的提示内容 | String | 暂无数据 |
