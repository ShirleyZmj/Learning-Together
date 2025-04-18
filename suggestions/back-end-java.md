# 后端
## 对于后端初学者学习路线建议

### 粘粘分享
我起步的时候是奔着后端所以先学了java的，我看网上说java目前岗位最多，虽然go好像性能比java更强，很多大厂也开始趋向于用go，但是说是用go的还是面积比较窄，所以刚入门网上还是建议说学java。说是在国内的话一定要学到微服务才有机会找到工作。  

[B站黑马Java学习路线](https://www.bilibili.com/opus/494817843530680807)  
我学习的路线基本就是跟着B站黑马走的，他们路线画的很清楚可以参考，我自己学的路线如下 
- java语法，还要学反射，多线程那些（我当时这块没认真学，后来做项目遇到以这块为基础的封装都很云里雾里）
- Springboot框架（SSM框架） 
- 做个CRUD单体项目 
- 拆单体项目成分布式微服务 （我看网上很多岗位都会要求懂MessageQueue（RabbitMQ, Kafka）， docker 一般在微服务阶段的项目就都有涉及。 
- 另外我看很多岗位都要求还得会运维的东西 CI/CD之类的，目前我对这块还很懵逼，只知道可能大概要学什么jenkins 之类的东西，但是没看到什么好的教程。
- 还有AWS云服务，也经常在岗位描述上看到，应该也是和运维部署有关系，目前只知道EC2（我理解就是云上虚拟机，应该是要把项目部署在上面）和S3（存文件的）。这块也没看到什么好的教程。

### 贝贝分享
因为我是业务服务端开发，所以可以从业务开发的角度学习有这些建议：
1. 会用 JAVA / C++/ C 其中一门语言（其实还有很多其他的语言，这三种比较基础可以先学，如果不想学其实也可以直接学其他的语言，比如直接学go感觉也没啥问题）
2. 了解使用python/nodejs/ shell 其中一种脚本语言
3. 持久数据存储 ：MySQL\MongDB\TiDB\其他   至少会一个，其他的了解基本原理和其优势、使用场景（熟练掌握）
4. 缓存数据库：Redis\ES\ 其他 （redis基本是必会的）
5. 消息队列：Kafka、RabbitMQ 等其他消息队列
6. 数据结构、算法
7. 操作系统、网络知识、架构设计、设计模式（重要）
8. 微服务架构、了解rpc； 可以学习一下protobuf
9. 微服务治理：k8s (不是所有公司都会用，一般只有微服务数量很多,比如几百个，人工维护已经很麻烦的时候才会使用，因为其实也需要一定的学习和运维成本) --- [devOps运维](./dev-ops.md)方向需要学习

## 资料分享
### 优秀项目学习（跑起来看一下）by 81老师
1. https://github.com/pig-mesh/pig
2. https://github.com/renrenio/renren-fast-vue
3. https://github.com/yangzongzhuan/RuoYi

### 网站
- [小林图解计算机基础](https://xiaolincoding.com/)：计算机网络和系统相关的内容，还有一些后端的内容
- [Java进阶](https://doocs.github.io/advanced-java/#/): 互联网 Java 工程师进阶知识完全扫盲

### PDF
[书本资源](../materials/java/index.md)

### 系统设计（国外大厂经常考）
1. [Alex Xu系统设计](https://github.com/mukul96/System-Design-AlexXu/blob/master/System%20Design%20Interview%20An%20Insider%E2%80%99s%20Guide%20by%20Alex%20Xu%20(z-lib.org).pdf)

## 问答集锦
1. 如何暴露服务，也就是如何让别人调用你的服务？  
- 如何暴露服务，其实就是把服务部署上去，然后开个端口暴露服务，然后就能通过ip:port访问服务。但我们一般不会想要暴露自己的服务器ip。所以一般会通过域名访问，可能再加个nginx转发。 要学习的话可以先试着买个便宜的服务器，搞一下。

2. 设计模式（重要）  这个有什么课或者学习方向的吗？ 
- 其实可以看 6大设计原则先 23种设计模式 都是这6大原则的扩充
- [六大设计原则](https://blog.csdn.net/Allen202/article/details/143231363)

3. 哪里有便宜的服务器
- [bandwagonhost](https://bandwagonhost.com/) 还可以看看这里还有没有19.9刀的
- 可以看下亿速云，华为啥的，这种基本上都有试用和首单优惠


