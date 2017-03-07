# EventBus
EventBus事件总线

EventBus是一款针对Android优化的发布/订阅事件总线。主要功能是替代Intent,Handler,BroadCast在Fragment，Activity，Service，线程之间传递消息.优点是开销小，代码更优雅。以及将发送者和接收者解耦

1. Publisher是发布者， 通过post()方法将消息事件Event发布到事件总线
2. EventBus是事件总线， 遍历所有已经注册事件的订阅者们，找到里边的onEvent等4个方法，分发Event
3. Subscriber是订阅者， 收到事件总线发下来的消息。即onEvent方法被执行。注意参数类型必须和发布者发布的参数一致。

依赖关系
compile 'org.greenrobot:eventbus:3.0.0'
