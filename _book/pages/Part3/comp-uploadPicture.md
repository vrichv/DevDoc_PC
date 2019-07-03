### [组件]UploadPicture 头像上传

组件路径 <em>src/components/File/UploadPicture.vue</em>，用于用户头像上传、单张轮播图上传等等。

![UploadPicture 附件上传](../../img/eg-uploadPicture.jpg ' UploadPicture 附件上传')

#### 使用示例

```javascript
<UploadPicture :uploadData="uploadData" @handleAvatarSuccess="handleAvatarSuccess" handleAvatarSuccessFun="handleAvatarSuccess"></UploadPicture>
<script>
	import UploadPicture from '@/components/File/UploadPicture' // 引入组件
	components: {UploadPicture} // 注册组件
</script>

```

<strong>【必填】</strong><em>uploadData</em>：类型【object】，要上传的数据对象。

<strong>【必填】</strong><em>handleAvatarSuccess</em>：文件上传成功时的钩子。

<strong>【必填】</strong><em>handleAvatarSuccessFun</em>：往 UploadPicture 组件传递的要执行的方法名，因为可能一个页面存在多个此组件，需要执行不同的方法。

```javascript
dataModel: {
 action: window.SITE_CONFIG['apiURL'] + '/sys/oss/upload', // 上传接口地址
 imageUrl: '', // 上传成功后的图片地址
 headers: { 'token': Cookies.get('token') } // 用于验证的token
}
```

#### UploadPicture Methods 附件上传方法

```javascript
// 附件上传成功后
// res：上传成功后后台返回来的数据
// file：上传成功后后台返回来的附件的信息数据
handleAvatarSuccess (res, file) {
  if (res.code === 0) {
    this.dataForm.pictureUrl = res.data.src // 获取到附件的地址用于验证
    this.uploadData.imageUrl = URL.createObjectURL(file.raw) // 获取到附件的地址用于保存
  } else {
    this.showMsg(500, `文件上传失败!`)
    return false
  }
}
```
