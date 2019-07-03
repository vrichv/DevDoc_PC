### publicJS 公用方法文件

文件路径 <em>src/assets/js/publicJS.js</em>，此文件内的所有方法均基于 Vue 的【[开发插件](https://cn.vuejs.org/v2/guide/plugins.html#ad '开发插件')】功能开发，并已全局注册。后续若有公用 dom 操作类方法，请在此文件内开发。

<strong>【强制】</strong>在封装某个功能在封装某个功能前，请先全局搜索查看是否已存在类似方法，若存在类似方法，尽量优化、完善旧方法。封装新方法时，请务必写清楚此方法的用途、徐传递的参数及参数说明。

```javascript
// 封装一个方法示例
// 此方法用于****
// field1：字段1，field2：字段2
Vue.prototype.functionName = function (field1,field2) { }

// 在页面中使用此方法
this.functionName(field1,field2) { }
```
