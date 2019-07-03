### 文档说明

目前（2019 年）此规范文档适用于公司购买的**人人开源**框架，此前所开发的燃气、热力等项目框架不适用此规范。后续若公司更换框架或框架升级，将会在[更新历史]()栏目进行说明，遇到的问题和解决方法将记录在[问题列表]()中。

**【重要】** 此文档目前托管在 github 上，账号：sdjcwx，密码：咨询薛猛

- 开发环境：node8.x 以上；Vue2.0+；Element2.0+
- 人人开源：[人人开源](https://www.renren.io/guide#fornt '人人开源前端部署')
- Vue 官网：[Vue-2.5.17](https://cn.vuejs.org/ 'Vue2.0+')
- Element：[Element-2.9.1](http://element-cn.eleme.io/#/zh-CN/component/installation 'Element')
- 文档地址：[GitHub](https://github.com/hiwebliu/DevDoc_PC) [内网地址](http://192.168.0.84:4000/)

### 文档文件说明

为方便此文档的后续人员维护，在此记录所用到的设置和插件。此文档基于**GitBook 程序**开发，用的**MarkDown**语法书写。

**【重要】** 此文档中所有可下载的资源文件，都存放在 28 的 ftp 文件目录内，可[点击跳转](ftp://192.168.0.28)直接打开 ftp，或按说明需求下载。

- book.json 文件：[[点击下载]](ftp://192.168.0.28/%C7%B0%B6%CB%BF%AA%B7%A2%CE%C4%B5%B5/PC%B6%CB/%D7%CA%D4%B4/book.json) 包含基础设置和所用到的插件
- website.css 文件：[[点击下载]](ftp://192.168.0.28/%C7%B0%B6%CB%BF%AA%B7%A2%CE%C4%B5%B5/PC%B6%CB/%D7%CA%D4%B4/website.css) 自定义了一些 gitbook 的样式
- MarkDown 语法：[[在线预览]](http://caibaojian.com/gitbook/format/markdown.html)

![资源文件位置](../../img/ziyuanjietu.png '线形图标库')

安装完 GitBook 程序后，覆盖目录下的**book.json 文件**文件，按以下命令执行即可。

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

| 项目         |          负责人           | 内容                                 |
| ------------ | :-----------------------: | ------------------------------------ |
| 此文档维护   |           刘振            | 根据框架的升级、更换来维护此文档     |
| UI 设计规范  |      王帅 王荣 田苗       | 设计公司项目的各类 UI 相关内容       |
| 前端开发规范 |           刘振            | 制定、规范前端相关的组件和代码规范   |
| 公用方法封装 | 刘振 刘书阳 庞春磊 赵世俊 | 封装、优化项目中公用的各类方法和组件 |
