teamdisk
========

基于webdav协议的云盘，企业盘解决方案。可创建企业或者团队自己的服务端存储。

同时使用tidesdk打包的全平台客户端app,可以让你随时随地方便的使用客户端参看服务端数据。

本程序分为3个部分

### 服务端webdav程序

代码在目录 /webdav_server

程序是基于sarbdav来开发的，通过PHP来做webdav服务器的模拟。同时我们加入了权限模块，管理员可以添加组，同时为这些组分配文件夹的使用权限。

当普通用户使用webdav客户端软件来读取服务端数据的时候，他只能看到管理员给他分配的资源。


### 管理员后台管理和资源服务操作api

代码在目录 /admin_and_api

这部分的程序是管理员后台操作模块，管理可通过后台为用户创建账号，添加组以及为他们分配权限等等用户管理操作。

管理员所有的变更都是通过api来完成，目前开发了管理员使用的用户管理api，文件夹api。有新的业务场景可以扩展这些api。以及提供用户使用的api

### 客户端程序

客户端使用html5开发，采用的是tidesdk打全平台的包，因此只用维护一套程序，即可完成ios,android,PC上的客户端APP

H5客户端，实现对webdav服务端文件的操作，包括复制，删除，下载等操作。

关于tidesdk的资料可以参考官网http://www.tidesdk.org/

![客户端图片](https://github.com/chenfan/teamdisk/blob/master/teamdisk_pc.jpg)


