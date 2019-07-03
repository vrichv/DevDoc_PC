### [组件]UploadFile 附件上传

组件路径 <em>src/components/File/UploadFile.vue</em>，用于添加项中上传图片、文档、视频等各类附件。

![uploadFile 附件上传](../../img/eg-uploadfile.png ' uploadFile 附件上传')

#### 使用示例

```javascript
<UploadFile :fileData='dataModel' :isView="true"></UploadFile>
<script>
	import UploadFile from '@/components/File/UploadFile' // 引入组件
	components: {UploadFile} // 注册组件
</script>

```

<strong>【必填】</strong><em>fileData</em>：类型【object】，一个上传附件对象，一个页面可能存在多个上传附件，需对应多个不同的 dataModel。

<strong>【选填】</strong><em>isView</em>：为 true 时，调用附件查看组件，只能查看附件不能上传。

```javascript
dataModel: {
	ref:'dataModelFileRef' // 当前上传附件的标识符，若一个添加页面存在多个上传模块，必须填不同名称
	title: '', // 附件标题
	limit: 4, // 限制最多上传附件4个
	accept: '', // 限制上传附件类型，此属性不填默认为：.jpg,.jpeg,.png,.gif,.bmp,.mp3,.mp4,.txt,.doc,.docx,.pptx,.ppt.,xls,.xlsx,
	fileSize: 5, // 限制单个附件体积大小不超过5M，此属性不填默认最大999M
	fileList: [ // 用于存储已选择的附件；若存储修改操作时后台传过来的已存在的附件信息
		{
			name: '1.jpg', // 已存在附件的名称
			url: './img/1.jpg' // 已存在附件的地址
		}
	]
}
```

#### UploadFile Methods 附件上传方法

```javascript
// 手动提交附件
// id：关联此附件所在添加页面保存后返回的ID
submitUpload (id) {}

// 此方法使用示例：
dataFormSubmitHandle: debounce(function () { // 提交表单
	this.$http().then(({ data: res })=>function(){
		if(res.code !== 0){
		}else {
			submitUpload (res.id) // 提交附件
		}
	}).catch(() => { })
}
```
