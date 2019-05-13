create database hope default character set utf8mb4 collate utf8mb4_unicode_ci

SUDO MAKE test
sudo make install
redis-server
 mac下安装redis

　　redis的介绍这里就不多说了,请参加博客windows下的mac安装,下面就直奔主题.

一.redis安装

1.首先,redis的默认端口为6379

2.下载mac版redis安装包,下载地址https://redis.io/download,我下载的版本是4.0.9

3.按顺序进行下列步骤:

解压:　　tar zxvf redis-4.0.9.tar.gz

移动到:　　mv redis-4.0.9.tar.gz /Users/panyang/　　此步如果不需要可以省略

　　我在解压的时候直接解压到当前目录了,所以不需要移动,就把这一步跳过了

切换到:　　cd /Users/panyang/redis-4.0.9/　　

　　进入到解压后的文件夹下面,路径改成你自己的文件夹存放的路径

编译测试:　　sudo make test

编译安装:　　sudo make install

二.redis的启动与停止

1.启动

redis-server,出现如下图就是启动成功了


----------------------------------------


https://github.com/java-aodeng/hope-plus



🇨🇳简体中文 | 🇺🇸English | 更新日志 | 版本🏷0.7.0
简介：

Hope-plus是我学习过程中诞生的，算我学习的结晶吧。主语言[java]

    项目地址： https://github.com/java-aodeng/hope-plus

模块划分
模块 	释义
hope-admin 	后台管理模块
hope-core 	核心业务类模块
hope-framework 	框架模块,提供数据操作,工具处理,通用Mapper,通用Service等
hope-sso-server 	单点登录-认证中心模块，支持集群
hope-generator 	代码生成模块-提供sql生成代码
hope-flyway 	数据库版本管理工具模块
使用说明(请仔细看,看不懂也不要来问我哦！！！)

# 1.使用命令拉取代码：
    git clone https://github.com/java-aodeng/hope-plus.git
# 2.创建数据库（取名）：hope， 字符集：utf8mb4;（注意：只需要你创建数据库即可，字符集不是utf8，而是utf8mb4）
# 3.使用IDEA导入该项目
# 4.修改配置
    A.打开hope-flyway模块，配置数据库连接:
        spring:
          datasource:
              url: 你的数据库地址
              username: 你的数据库用户名
              password: 你的数据库密码
    B.打开hope-admin模块，配置数据库连接和redis连接:
        a.数据库配置(可搜索datasource或定位到L.17)
        b.redis配置(可搜索redis或定位到L.29,注：该项目必须安装redis服务才能启动)
# 5.运行项目(数据库管理模块)
    a.直接运行hope-flyway目录下的HopeFlywayApplication.java
    b.查看数据库是否自动生成表和初始化的数据
# 6.运行项目(后台管理模块)
    a.直接运行hope-admin目录下的HopeAdminApplication.java
    b.浏览器访问：http://127.0.0.1:8886
# 7.运行项目(单点登录模块)
    a.直接运行hope-sso-server目录下的HopeSsoServerApplication.java
    b.浏览器访问：http://127.0.0.1:8887
# 8.运行项目(代码生成模块)
    a.直接运行hope-generator目录下的HopeGeneratorApplication.java
    b.浏览器访问：http://127.0.0.1:8888

账号

后台登录：账号：admin 密码：123456

资源监控：账号：hope-druid 密码：hope-druid

后端API管理：localhost:8886/swagger-ui.html
感谢：

Hope-plus的诞生离不开下面这些项目（取之开源，用之开源）：

    Spring Boot：核心框架
    Apache Shiro：权限框架
    Redis：缓存框架
    Thymeleaf：模板引擎
    MyBatis：用于Java的MyBatis SQL Mapper框架
    PageHelper：分页插件
    tk.mybatis：通用Mapper
    alibaba/druid：数据库连接池
    alibaba/fastjson：用于Java的快速JSON解析器/生成器
    shiro-redis：一个可以由shiro使用的redis缓存工具
    Lombok：让代码更简洁
    Hutool：一个Java工具包，也只是一个工具包，它帮助我们简化每一行代码，减少每一个方法，让Java语言也可以“甜甜的”
    Bootstrap：使用最广泛的前端 ui 框架
    JQuery：使用最广泛的 JavaScript 框架
    Layer：弹出层组件
    kaptcha：Google验证码
    jrebel：热部署
    swagger：Swagger（丝袜哥）是世界上最流行的 API 表达工具。

