# 远程客户端VS本地客户端

正如我们在这章前面看到的，我们的客户端是通过接口来定义的。添加这样一层的主要动机在于，我们可以用远程实现来代替本地实现。让我们一起看下A依赖B的情况。如果这些部分部署在单独的服务器上，我们要使用B的客户实现的话将导致远程调用。然而，如果两个部分共存在一个JVM上，使用远程客户端将导致不必要的网络延迟。使用客户端代替直接调用B部分实现保证了没有网络花费，这样减少了延迟。

### 注意
这部分都是使用的微架构，微架构（<https://en.wikipedia.org/wiki/Microservices>）现在变得非常流行了。这种架构方式将复杂应用打碎成小的独立的部分。