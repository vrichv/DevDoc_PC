### [组件]Tree 树形控件

组件路径 <em>src/components/File/Tree/Tree.vue</em>，Tree 树形控件用于展示存在上下级逻辑的数据

![Tree 树形控件](../../img/eg-tree.png ' Tree 树形控件')

#### 使用示例

```javascript
<componentsTree :treeData="typeTreeData" ref="typeTreeComponent" treeNodeKey="id"> </componentsTree>
<script>
	import componentsTree from '@/components/Tree/Tree' // 引入组件
	components: {componentsTree} // 注册组件
</script>

```

<strong>【必填】</strong><em>treeData</em>：树装结构的数据来源

<strong>【必填】</strong><em>ref</em>：此树状控件标识符，一个页面可能存在多个树，通过此 ref 区分

<strong>【必填】</strong><em>treeNodeKey</em>：树状节点的唯一标识符

```javascript
待修改
```

#### Tree Methods 树形控件方法

```javascript
// 清空所有选中==一般查询重置时父组件直接调用
this.$refs.modelTree.setCheckedKeys([])

// 此方法用法：
// 父级页面通过组件ref调用
this.$refs[refName].clearAllChecked()
```
