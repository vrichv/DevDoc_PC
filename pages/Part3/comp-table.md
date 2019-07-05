### [组件]Table 表格

<p>组件路径 <em>src/components/Table/Table.vue</em>，最常用的用于展示多条结构类似的数据，可对数据进行排序、筛选、对比或其他自定义操作。</p>

![Table 表格示例](../../img/eg-Table.png 'Table 表格示例')

#### 使用示例

```vue
<table :data="dataModel"></table>
```

<strong>【必填】</strong><em>dataModel</em>：类型【object】，要展示的一个表格的数据对象，一个页面可能存在多个数据表格，所以需要配置此对象内的不同参数。包含参数如下：

```javascript
dataModel {
	addVisible: false, // 此表格的添加页面初始可视化状态
	addref: 'dataModelAdd', // 此表格的添加页面的ref标识符
	view: false, // 此表格的添加页面初始可视化状态
	viewref: 'dataModelView', // 此表格的添加页面初始可视化状态
	mixinViewModuleOptions{ // 此表格的必要初始属性
		getDataListURL: '/demo/news/page',  // 请求数据的接口地址
		deleteURL: '/demo/news' // 删除数据的接口地址
		getDataListIsPage: false  // 数据列表接口，是否需要分页，默认为true不需要填写，只需不分页时填写为false即可
		deleteIsBatch: false, // 删除接口，是否需要批量，默认为true不需要填写，数据表格为单选时填写为false即可
		deleteIsBatchKey: 'id', // 删除接口，批量状态下由那个key进行标记操作？比如：pid，uid...
		exportURL: '', // 导出接口，API地址
		dataForm: {}, // 页面中的查询条件，比如包含title、pubDate等等
  },
	tableData: [],  // 存储请求后的数据

	tableColumn: [// 一列数据的属性参数
		{
			fixed: 'left',  //  是否固定列，left,right
			type: 'selection', // 列的类型，selection(多选)/index(索引)/expand(展开项)
			label: '标题',  // 显示的标题
			prop: 'title', // 对应列内容的字段名
			sortable: true, // 对应列是否可以排序
			width: '400', // 对应列的宽度
			isTip: true, // 当内容过长被隐藏时显示 tooltip
			formatter: 'formatterFunName' // 对此栏的值进行格式化，比如性别如果是0和1，可以经过格式化后返回为男和女
		},
  ],

	tableOption: { // 针对每一行数据要进行的操作栏
		fixed: 'right',
		options: [
			{
				label: '删除', // 操作的label内容
				methods: this.deleteHandle, // 要执行的方法
				hasPermission: 'customPages:model2:delete' // 按钮的权限标识符
			}
		]
	}
}
```

#### Table Methods 表格方法

```javascript
// 获取当前表格点击的当前行的数据
getCurrentRow () {
	console.log(this.dataModel.currentRow)
},
// 获取当前多选表格的选中行的数据
getCurrentRows () {
	console.log(this.dataModel.currentRows)
},
// 根据某一行的某个字段判断，来高亮当前行
tableRowClassName ({ row, rowIndex }) {
	if (row.title === 'AAA') {
		return { id: rowIndex, className: 'warning-row' }
	} else if (rowIndex === 3) {
		return { id: rowIndex, className: 'success-row' }
	}
},
// 格式化性别
formatSex (val) {
  return val === '0' ? '男': '女'
},
```
