##简介

### Apache Kafka是一个分布式流处理平台，准确的讲它到底是什么？

一个流处理平台有三个关键功能：

* 发布和订阅消息流，类似于消息队列或企业消息传递系统。
* 高容错率的持久化消息流
* 处理发生的消息流

Kafka通常用于两大类应用：

* 构建可在系统或应用程序之间可靠获取数据的实时流数据管道
* 构建转换或响应数据流的实时流应用程序

要了解Kafka如何做这些事情，让我们深入探讨Kafka的能力。

首先是几个概念：

* Kafka作为一个集群运行在一个或多个可跨多个数据中心的服务器上。
* Kafka集群以`topic`类别存储`records`
* 每一个`record`包含一个`key`,一个`value`,一个`timestamp`

Kafka有四个核心的APIs:

* `Producer API`允许一个应用发布记录流到一个或多个Kafka `topics`
* `Consumer API`允许一个应用订阅多个`topics`(主题),并处理这些记录
* `Streams API`允许应用程序充当流处理器，消费来自一个或多个`topics`的消息，并输出到一个或多个`topics`
* `Connector API`允许建立一个将 Kafka `topics`连接到系统或者数据平台的可重用`producer`或`consumer`，。例如，一个关系型数据库的连接器可以捕捉到每个表的变化

Client和Server之间的交流通过一条简单、高性能并且不局限某种开发语言的TCP协议。

### Topics and Logs