### [组件]baiduMap 百度地图

组件路径 <em>src/components/Maps/BaiduMap.vue</em>，基于【[Vue Baidu Map](https://dafrok.github.io/vue-baidu-map/#/zh/start/installation 'Vue Baidu Map')】组件的二次开发，后续添加相关百度地图功能，请先按照此组件的文档说明进行开发。

![baiduMap 百度地图](../../img/eg-baiduMap.png ' baiduMap 百度地图')

#### 使用示例

```javascript
<baiduMap :mapData='dataModel' ref="baiduMap" @FunGetPoint="getPointGT($event)"></baiduMap>
<script>
	import baiduMap from '@/components/Maps/BaiduMap' // 引入组件
	components: {baiduMap} // 注册组件
</script>

```

<strong>【必填】</strong><em>mapData</em>：类型【object】，传给组件的一个包含经纬度的数据对象

<strong>【必填】</strong><em>ref</em>：此组件的标识符，用于一些基于此标识符的操作

<strong>【必填】</strong><em> @contentChangeFun</em>：通过此方法获取组件返回来的经纬度数据

```javascript
dataModel： {
	lng: '', // 经度
	lat: '' // 纬度
}
```

#### baiduMap Methods 百度地图方法

```javascript
// 接收地图子组件返回来的地图上点的经纬度
getPointGT (res) {
	this.dataForm.lng = res.lng
	this.dataForm.lat = res.lat
}
```
