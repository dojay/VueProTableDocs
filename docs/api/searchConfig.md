#### searchConfig是搜索部分的数据配置部分，它是一个数组，如下示例：

``` html
<template>
  <VueProTable
    :searchConfig="searchConfig"
  ></VueProTable>
</template>

<script>
  export default {
    data() {
      return {
        searchConfig: [
          {
            type: 'input',
            label: '订单号',
            key: 'orderNo'
          },
          {
            type: 'select',
            label: '订单状态',
            key: 'orderStatus',
            options: [
              {key: '1', value: '进行中'},
              {key: '2', value: '已完成'}
            ]
          },
          {
            type: 'datepicker',
            label: '开始时间',
            key: 'startDate',
            defaultVal: ''
          }
        ]
      }
    }
  }
</script>
```

#### 公共配置项

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| type | 搜索框类型, 可选值有input, select, datepicker, timepicker | String | input |
| label | 搜索框label | String | - |
| key | 搜索框的v-modal | String | - |

##### Input配置

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| inputType | 输入框类型，可选值为 text、password、textarea、url、email、date、number、tel | String | text |
| placeholder | 占位文本 | String | - |
| clearable | 是否显示清空按钮 | Boolean | false |
| disabled | 设置输入框为禁用状态 | Boolean | false |
| readonly | 设置输入框为只读 | Boolean | false |
| maxlength | 最大输入长度 | Number | 140 |
| prefix | 输入框头部图标 | String | - |
| number | 将用户的输入转换为 Number 类型 | Boolean | false |

##### Select配置

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| multiple | 是否支持多选 | Boolean | false |
| clearable | 是否显示清空按钮 | Boolean | false |
| disabled | 设置输入框为禁用状态 | Boolean | false |
| filterable | 是否支持搜索 | Boolean | false |
| placeholder | 占位文本 | String | - |
| placement | 弹窗的展开方向，可选值为 top、bottom、top-start、bottom-start、top-end、bottom-end | String | bottom-start |

##### DatePicker配置

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| dateType | 显示类型，可选值为 date、daterange、datetime、datetimerange、year、month | String | date |
| format | 展示的日期格式 | Date | yyyy-MM-dd |
| disabled | 设置输入框为禁用状态 | Boolean | false |
| placeholder | 占位文本 | String | - |
| placement | 弹窗的展开方向，可选值为 top、bottom、top-start、bottom-start、top-end、bottom-end | String | bottom-start |
| show-week-numbers | 开启后，可以显示星期数。 | Boolean | false |
| start-date | 设置默认显示的起始日期。 | Date | - |
| options | 选择器额外配置，比如不可选日期与快捷选项，具体项详见下表 | Object | - |
| clearable | 是否显示清除按钮 | Boolean | false |
| readonly | 完全只读，开启后不会弹出选择器，只在没有设置 open 属性下生效 | Boolean | false |

options

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| disabledDate | 设置不可选择的日期，参数为当前的日期，需要返回 Boolean 是否禁用这天 | Function | - |
