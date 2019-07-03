### mixins.js 混入文件

文件路径 <em>src/mixins/mixins.js</em>，采用 Vue 的混入文件机制，将框架中通用的属性、方法等放到此文件中，可在所有页面中混入公用属性和方法，比如常用的增删改查、导入导出等等。具体说明请参考官方文档【[Vue 的混入说明](http://https://cn.vuejs.org/v2/guide/mixins.html#ad 'Vue的混入说明')】

所有的列表页面都需要引用此文件，使用方法：

```javascript
import mixins from '@/mixins/mixins' // 引入
export default {
  mixins: [mixins] // 注册混入文件
}
```

目前封装的公用方法如下，后续若有通用数据处理类方法，请放到此文件中。

```javascript
// 获取数据列表
// obj 是传过来的查询对象， 包含接口地址、 各类配置等
getDataList (obj) {
	// 注意：所有页面的获取数据，必须在vue声明周期的created中执行
	//  creaated () {getDataList (obj)}
}

// 新增 / 修改
// id：如果为undefined，就是修改功能
addOrUpdateHandle (obj, id) {}

// 删除
deleteHandle (obj, id) {}

// 导出
exportHandle (obj) {}

// 查看
viewHandle (obj, id) {}
```
