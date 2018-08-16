
项目名称: WE_CHAT
开发工具: Linux 下vim编译器
数据库: Mysql
项目简介：
项目功能架构：
 1. 采用client/server模式；
 2. 服务器采用半同步/半反应堆模式
 3. 采用线程池缓解缓解并发压力
 2. 客户操作主界面（注册、登陆、帮助、退出）、登录后主界面（查看在线列表、私聊、群聊、查看聊天记录、退出）；

##server##

###include###
 1. config.h：      服务器端配置文件(变量定义、函数声明);
 2. connMysql.h:    数据库相关头文件及函数;
 3. threadPool.h:   线程池相关头文件及函数;
###source###
 1. threadPool.c:   线程池相关操作；
 2. config.c：      服务器端共用函数的实现文件；
 3. server.c：      服务器端主程序代码；
 4. list.c：        用于维护在线用户的添加、更新、删除操作；
 5. register.c：    服务器端处理用户注册；
 6. login.c：       服务器端处理用户登录；
 7. chat.c：        服务器端处理用户的聊天请求；
 8. handleConn.c:   处理客户端连接请求相关函数；
 9. connMysql.c:    连接数据库相关函数；

##client##

###include###
 1. config.h：      客户端配置文件；
###source###
 1. nonBlockConn.c: 设置非阻塞超时connect；
 2. config.c：      客户端共用函数的实现文件；
 3. client.c：      客户端主程序代码；
 4. register.c：    客户端实现用户注册；
 5. checkpasswd.c:  客户端检查代码的；
 6. login.c：       客户端实现用户登录；
 7. chat.c：        客户端实现用户的聊天功能；
 8. interface.c：   客户端界面文件；
 9. makefile：      客户端编译多文件；

