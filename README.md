# ScoreMarker2.0

##### 此版本采用spring整合RabbitMQ的方式，在1.0版本的基础上，进行了整体的代码重构。
##### 相对于1.0版本所采用的安装为mq-server的消息队列部署服务的形式，2.0版本有以下优势：
>1. 极大程度地避免了原mq-server服务由于未对ack消息确认机制未作处理，当消息消费端不断地因网络或其他原因导致消息消费失败，所造成的内存泄漏、服务器宕机，进一步造成的前后台系统通知瘫痪问题；
>2. 本服务独立出来，成为专门的系统同前后台系统一样部署在web容器中，可以实现代码动态更新及热部署；
>3. 达到了整体系统的代码松耦合效果。