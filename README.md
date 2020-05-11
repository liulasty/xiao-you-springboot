# 校友管理系统部署说明

> 线上访问地址（后台）：localhost:9200
>
> 线上访问地址（前台）：localhost:9100/index

## 本地部署

1.在mysql中新建数据库xiaoyou，将xiaoyou.sql导入该数据库。

2.打开IDEA，导入此项目， 打开xiaoyou3\xiaoyou_manage\src\main\resources\application.yml
和xiaoyou3\xiaoyou_index\src\main\resources\application.yml的配置文件，
修改数据库用户名和密码为自己本地数据库的用户名和密码，修改数据库地址为本机的对应数据库地址如下：

```yaml
spring:
  datasource:
#数据库地址
    url: jdbc:mysql://localhost:3306/xiaoyou?serverTimezone=GMT%2B8
    type: com.alibaba.druid.pool.DruidDataSource
#mysql的账号
    username: root
#mysql的密码
    password: root
    driver-class-name: com.mysql.jdbc.Driver
```

3.运行xiaoyou3\xiaoyou_index\src\main\java\com\lgy\xiaoyou_index\下的XiaoyouIndexApplication.java类，启动前台。

4.运行xiaoyou3\xiaoyou_manage\src\main\java\com\lgy\xiaoyou_manage\下的XiaoyouManageApplication.java类，启动后台。

5.打开浏览器，输入 localhost:9200 进入后台登录界面；输入localhost:9100/index进入前台首页。

6.输入用户名和密码访问系统。
	

## 运行说明

### 1.运行环境：

​	JDK1.8；Tomcat9.0；MySQL5.5

### 2.账号密码：

管理员账号： 111

管理员密码：  123

普通用户账号：2020

普通用户密码：2020

### 3.访问：

在启动之后访问localhost:9200进入后台登录界面，输入管理员账户名密码进行登录，登录成功便可使用后台系统；访问localhost:9100/index进入前台首页，点击右上角登录按钮，输入普通用户账户名密码进行登录，成功即可使用前台。

## 系统展示

### 1.前台

![前台界面](https://gycode.oss-cn-qingdao.aliyuncs.com/gycodeImg/20200511225515.png)



### 2.后台

![后台](https://gycode.oss-cn-qingdao.aliyuncs.com/gycodeImg/20200511225641.png)

![部分系统截图1](https://gycode.oss-cn-qingdao.aliyuncs.com/gycodeImg/20200511225728.png)

![部分系统截图2](https://gycode.oss-cn-qingdao.aliyuncs.com/gycodeImg/20200511225849.png)
