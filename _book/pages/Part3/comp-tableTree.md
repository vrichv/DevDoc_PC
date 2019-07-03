### [组件]TableTree 表格树

<p>组件路径 <em>src/components/Table/TableTree.vue</em>，表格中的数据以树状形式展示，存在上下级的数据关系。</p>

![TableTree 表格树示例](../../img/eg-TableTree.png 'TableTree 表格树示例')

#### 使用示例

```vue
<treeTable :data="dataModel" treeTableRowKey="id">
```

<strong>【必填】</strong><em>dataModel</em>：类型【object】，要展示的一个表格的数据对象，一个页面可能存在多个数据表格，所以需要配置此对象内的不同参数。包含参数和组件 Table 表格相同，请参考 Table 表格组件的参数说明。

<strong>【必填】</strong><em>treeTableRowKey</em>：行数据的 Key

#### TableTree Methods 表格树方法

```javascript
// 获取当前表格点击的当前行的数据
getCurrentRow () {
	console.log(this.dataModel.currentRow)
}
```
