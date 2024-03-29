




<h1 class="heading"><span class="name">RemotePort</span></h1>

Applies To: [TCPSocket](../a-z/tcpsocket.md)


**Description**


The RemotePort property is a scalar integer in the range 1-65536 that identifies the [port number](../Miscellaneous/Port Number.htm) associated with a service on a remote computer.


RemotePort may only be specified by a client [TCPSocket](../a-z/tcpsocket.md) that is intended to make a connection with a server. Furthermore, it must be specified in the `⎕WC` statement that creates the [TCPSocket](../a-z/tcpsocket.md) object and it may not subsequently be changed using `⎕WS`.


Note that you may use *either* RemotePort *or* [RemotePortName](../a-z/remoteportname.md) to identify the remote service. If you know the port number, it is normally quicker to specify RemotePort. However unless it is a *well known port number*, the use of a port name is generally more flexible. If you specify both properties, the value of [RemotePortName](../a-z/remoteportname.md) will be ignored.


For a server [TCPSocket](../a-z/tcpsocket.md), RemotePort is determined by the [port number](../Miscellaneous/Port Number.htm) of the connecting process and is a read-only property.



