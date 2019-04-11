### 文档说明

目前（2019年）此规范文档适用于公司购买的**人人开源**框架，此前所开发的燃气、热力等项目框架不适用此规范。后续若公司更换框架或框架升级，将会在[更新历史]()栏目进行说明，遇到的问题和解决方法将记录在[问题列表]()中。

* 开发环境：node8.x以上；Vue2.0+；Element2.0+
* 人人开源：[人人开源](https://www.renren.io/guide#fornt "人人开源前端部署")
* Vue官网：[Vue2.0+](https://cn.vuejs.org/ "Vue2.0+")
* Element：[Element2.7.0](http://element-cn.eleme.io/#/zh-CN/component/installation "Element")
* 文档地址：[GitHub](https://github.com/hiwebliu/DevDoc_PC)  [内网地址](http://192.168.0.84:4000/)

### 文档文件说明

为方便此文档的后续人员维护，在此记录所用到的设置和插件。此文档基于**GitBook程序**开发，用的**MarkDown**语法书写。

* book.json文件：[[点击下载]](http://192.168.0.80:81/zentao/file-download-20465.html?zentaosid=hih7j7ccepof1j158g1k5gsi00) 包含基础设置和所用到的插件
* website.css：[[点击下载]](http://192.168.0.80:81/zentao/file-download-20486.html?zentaosid=70pir8dsskmdaecrcjph96irb6) 自定义了一些gitbook的样式
* MarkDown语法：[[在线预览]](http://caibaojian.com/gitbook/format/markdown.html)

安装完GitBook程序后，覆盖目录下的**book.json文件**文件，按以下命令执行即可。

```javascript
/ 安装文件中的插件
gitbook install 

/ 重新创建gitbook
gitbook build

/ 启动gitbook
gitbook serve

```


### 相关人员

<p>相关人员设计、制定内容后，在此文档中提交可预览或可下载的资源文件，后续所有项目开发需安装相关规范来进行设计和开发。新增内容或内容维护经公司审批后发布到此文档内。</p>

| 项目          | 负责人           | 内容  |
| ------------- |:-------------:| -----|
| 此文档维护      | 刘振           | 根据框架的升级、更换来维护此文档 |
| UI设计规范      | 王帅  刘振      |   设计公司项目的各类UI相关内容 |
| 前端开发规范     | 刘振           |   制定、规范前端相关的组件和代码规范 |
| 公用方法封装     | 刘振 翟金辉     |   封装、优化项目中公用的各类方法和组件 |


