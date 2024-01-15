本文描述了RDMA编程过程中的SEND-RECEIVE双边原语的代码实现,包含多个版本。<br>
1、client向server发送消息，server回复client收到消息(ACK)，然后两边断开连接。<br>
2、server端循环等待客户端建立连接，client发送一次消息后，双方断开连接。<br>
3、server端循环等待客户端建立连接，一旦建立，client端可以一直向server端发送消息，直到发送消息为disconnect，server和client断开链接，但是server此时仍然可以等待别的client发送消息。
