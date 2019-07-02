# page-foot
一个基于Element的Vue2插件

# 安装
```
npm install page-foot --save
或
cnpm insatll page-foot --save
```

# 使用
- 基于element-ui 请保证项目中全局引入了element-ui
- 在main.js中添加
```JavaScript
import PageFoot from 'page-foot'

Vue.use(PageFoot)
```
- 在Vue组件中使用
```JavaScript
<template>
  <div id="app">
    <page-foot :pagination="pagination" @page-change="handleCurrentChange" ></page-foot>
  </div>
</template>

<script>
export default {
  name: 'app',
  data: () => ({
    pagination: {
      current_page: 1,
      per_page: 10,
      total: 0
    }
  }),
  methods: {
    handleCurrentChange(val) {
      console.log(val)
    }
  }
}
</script>

<style>
</style>
```

# API使用
```JavaScript
<page-foot :pagination="pagination" @page-change="handleCurrentChange"></page-foot>

```

# 事件绑定
- [handleCurrentChange](https://element.eleme.cn/#/zh-CN/component/pagination)
```JavaScript
<page-foot @play="play"></page-foot>

export default {
    methods: {
      handleCurrentChange(val) {
        console.log('page change', val)
      }
    }
```
