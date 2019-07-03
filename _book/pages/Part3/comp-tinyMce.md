### [组件]TinyMce 文本编辑器

组件路径 <em>src/components/tinyMce/tinyMce.vue</em>，二次封装第三方富文本编辑器，能保存从 word 拷贝过来的文本格式。

![TinyMce 文本编辑器](../../img/eg-tinymce.png ' TinyMce 文本编辑器')

#### 使用示例

```javascript
<Editor :evalue="dataForm.content" contentChangeFun="contentChangeFun" @contentChangeFun="contentChangeFun"
></Editor>
<script>
	import Editor from '@/components/tinyMce/tinyMce' // 引入组件
	components: {Editor} // 注册组件
</script>

```

<strong>【必填】</strong><em>evalue</em>：用于存储编辑器内的内容

<strong>【必填】</strong><em>contentChangeFun</em>：给此组件传递的要执行的方法名

<strong>【必填】</strong><em> @contentChangeFun</em>：通过此方法获取编辑器返回的内容

```javascript
待修改
```

#### TinyMce Methods 文本编辑器方法

```javascript
// 获取编辑器返回的内容
contentChangeFun (val) {
	this.dataForm.content = val
},
```
