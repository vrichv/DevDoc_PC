### 框架使用说明

<strong>【重要】</strong>此文档中示例框架的 svn 地址：[右键复制地址](http://192.168.0.55:10001/svn/MECProduct/Code/js/vue_pc)。**用于新项目请复制一份，不要在此示例框架中修改！** 如果你是第一次用此框架和 java 环境，请点击下载：[java 框架所需文件.zip](ftp://192.168.0.28/%C7%B0%B6%CB%BF%AA%B7%A2%CE%C4%B5%B5/PC%B6%CB/%D7%CA%D4%B4/java%BF%F2%BC%DC%CB%F9%D0%E8%CE%C4%BC%FE.zip)，并按照以下顺序进行设置。

1. 此压缩包内包含：jdk(1.8)，IDEA，MAVEN(3.6.1)，若官网有新版本可从官网下载
2. 安装 JDK 并配置 JDK 环境：[WIN10 配置 JDK 教程](https://jingyan.baidu.com/article/db55b609fa946e4ba20a2f56.html)
3. 安装 IDEA，<em>resources_zh_CN_IntelliJIDEA_2018.3_r1.jar</em>是汉化文件，拷贝到 IDEA 安装目录/lib 下
4. 激活并配置 JDK：[IDEA 配置 JDK 教程](https://jingyan.baidu.com/article/bea41d43a3b5edb4c51be6b6.html)
5. IDEA 配置 Maven：[IDEA 配置 Maven 教程](https://blog.csdn.net/westos_linux/article/details/78968012)
6. <em>LocalWarehouse.zip</em>是第 5 条教程中所用到的 LocalWarehouse 文件资源，后续就不需要再下载了。
7. 修改后端数据库地址，文件路径：<em>security-enterprise/src/main/java/io/renren/AdminApplication.java</em>，#MySQL 下面的相关信息
8. 修改前端地址：<em>security-enterprise-admin/Public/index.html</em>里的[开发环境下]信息，默认是 localhost，即：用的本地后台服务。可改为 192.168.0.28:8080

![框架文件资源说明](../../img/ziyuanjietu1.png '框架文件夹')

- <em>security-enterprise</em>：后端代码文件，具体操作请阅读[security-enterprise 开发文档 2.2_专业版.pdf]
- <em>security-enterprise-admin</em>：前端代码文件，具体目录和文件说明请查看 [[框架资源说明]](ziyuanshuoming.md)，并按照规定操作。
