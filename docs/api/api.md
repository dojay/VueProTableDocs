#### 使用方法

``` html
<VueProTable
  :searchConfig="searchConfig"
  :tableParams="tableParams"
  :pageParams="pageParams"
  @search="searchList"
  @pageChange="pageChange"
></VueProTable>
```

#### API

##### Prop

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| searchConfig | 搜索框配置数据 | Array | [] |
| tableParams | 表格表头配置 | Object | null |
| pageParams | 分页信息 | Object | null |

##### Event

| 属性 | 说明 | 返回值 |
| --- | --- | --- |
| search | 点击按钮事件 | 搜索框的model |
| pageChange | 点击分页 | 页数 |
