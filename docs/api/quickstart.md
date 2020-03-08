## 快速上手

如果项目中没有使用iview并且不打算使用iview的话，请绕行。

如果想使用该组件，请先阅读[iview](https://iviewui.com/)的文档。

### 如何使用

1. 安装到项目中

``` shell
npm install VueProTable
# or
yarn add VueProTable
```

2. main.js中引用

``` js
  import VueProTable from 'VueProTable'

  Vue.use(VueProTable)
```

3. 页面中使用

```
<VueProTable
  :searchConfig="searchConfig"
  :tableParams="tableParams"
  :pageParams="pageParams"
  @search="searchList"
  @pageChange="pageChange"
/>
```

更多说明请看教程