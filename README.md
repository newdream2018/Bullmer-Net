# Bullmer-Net
Bullmer Server 

1.全部模块化设计，对线程池，buf池，异步事件/信号等进行了封装，设计良好，结构清晰，易于维护。 

2.很好的解决了数据包传输中出现的粘包，半包，组包问题，应用业务不用在考虑此类问题。 

3.较好的解决了在连接数量较多情况下易出现网络拥塞问题(生产者/消费者模式,xDispacher线程)。 

4.解决了在能多发连接时及时响应新的连接请求，且在客户端连接异常中断时及时响应做出处理，系统响应速度快，可靠性/稳定性良好，cpu低耗。

5.较好的解决了大数据的传输问题。 

6.采用跨平台设计方案，api编写，支持windows/iocp，linux/epoll，不依赖第三方库(系统必要的库初外)。 

7:能同时监听最多50个端口，压力测并发2000个连接，最大支撑连接数根据系统而定。 

8:充分利用cpu,及线程池,降低消耗，提高线程利用率:当前事务线程本次处理完毕会挂起到空闲堆栈，直到下一个事务请求被唤醒。
