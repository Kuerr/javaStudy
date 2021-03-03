### **maven**

#### 1、简介

###### 1）功能

简洁jar包的管理（下载）

管理依赖关系

面向过程，编译测试运行打包。

###### 2）过程（构建）：

1）清理：之前的项目编译的字节码文件清除

2）编译：编译程序中的Java文件，转换为字节码文件

3）测试：test文件

4）报告：测试报告

5）打包：项目中class、配置文件打包

6）安装：安装到本地仓库之中

7）部署：程序安装执行



###### 3）核心概念

1）POM（project object model）：项目对象模型，控制maven搭建构建的过程，管理jar依赖



* modelVersion ：maven版本

  

  坐标（gav）安装会根据这个建文件

* groupId：组织id，公司域名的倒写 

* artifacted：项目名称

* version：版本号

  

* packaging：打包后压缩文件的扩展名 

* dependencies：依赖 

* build：构建

  

2）约定的目录结构：maven目录和文件的位置

* 以文件夹形式存在

![image-20210223122612188](C:\Users\11625\AppData\Roaming\Typora\typora-user-images\image-20210223122612188.png)

​		main:存放主程序

​		test：存放

3）坐标：字符串

4）依赖管理：jar包之间的关系

5）仓库：资源存放，maven的插件jar包和项目的jar

**特点：向上获取资源 **

* 本地仓库：settings.xml之中的<localRepository>标签

* 远程仓库：中央仓库
* 私服：公司内部

6）生命周期：maven构建的过程

7）继承

8）聚合



#### 2、使用maven（3.3.9）

##### 1)安装 

maven：mvn -v 有显示即安装成功 ![	](C:\Users\11625\AppData\Roaming\Typora\typora-user-images\image-20210223121110422.png)

##### 2)约定的目录结构

以文件夹形式存在

![image-20210223122612188](C:\Users\11625\AppData\Roaming\Typora\typora-user-images\image-20210223122612188.png)

main:存放主程序

test：存放

##### 3）常用命令

* mvn compile ：编译，生成class文件，存放在target文件
* mvn clean
* mvn test-compile
* mvn test
* mvn package
* mvn 

#### 3、idea使用

###### Tip：不用idea内置的maven

使用模板创建项目：

1）maven-archetype-quickstart 

2）maven-archettype-webapp



#### 4、依赖范围

1）用scope来表示： compile/test/provided

![img](https://img-blog.csdnimg.cn/20191226230126381.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2xpc2h1b2JveQ==,size_16,color_FFFFFF,t_70)

compile：打包会带jar包

provided：不需要自带



自定义变量：在property进行设置全局变量。通过${}来引用。

在property 起到过滤的作用。

