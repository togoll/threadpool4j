threadpool4j
============

在软件架构和设计中，会尽可能地将操作`异步化`，缩短响应时间，提升性能。

将异步任务放入`线程池`，这是许多人都知道的。但是当异步任务多了之后，如果全放在同一个线程池执行，会出现一些问题：
* 不同任务因其执行的操作不同，所需时间不同。如果有大量执行时间较久的异步任务，会阻塞那些执行非常快的异步任务，导致原本很快可以完成的异步任务也变慢。
* 操作本地内容的异步任务和操作远程内容的异步任务。如果放在同一个线程池中，在网络出现故障的情况下，会出现大量的任务积压，导致执行本地内容的异步任务也受影响。

现实生活中，机动车行驶时，会根据行驶的速度划分超车道、快车道、慢车道和应急车道，避免速度慢的车辆阻塞速度快的车辆。

![车道划分](http://img0.ph.126.net/JgUtSzhdAatg_5B5mne0KQ==/6608414527631781351.png)

同理，将异步任务放入不同的线程池执行，就可以解决上面的两个问题。

`threadpool4j`是一个实现了`多线程池`的类库，其文档如下：

1、[编译threadpool4j](https://github.com/aofeng/threadpool4j/wiki/%E7%BC%96%E8%AF%91threadpool4j)。

2、[threadpool4j入门指南](https://github.com/aofeng/threadpool4j/wiki/threadpool4j%E4%BD%BF%E7%94%A8%E6%8C%87%E5%8D%97)。
