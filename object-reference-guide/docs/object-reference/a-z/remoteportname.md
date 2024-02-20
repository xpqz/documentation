




<h1 class="heading"><span class="name">RemotePortName</span></h1>

Applies To: [TCPSocket](./tcpsocket.md)


**Description**


The RemotePortName property is a character vector that specifies the port name of the remote service to which you wish to make a connection.



RemotePortName may only be specified by a client [TCPSocket](./tcpsocket.md) that is intended to make a connection with a server. Furthermore, it must be specified in the `⎕WC` statement that creates the [TCPSocket](./tcpsocket.md) object and it may not subsequently be changed using `⎕WS`.


When the specified port name has been resolved to a port number, the [TCPSocket](./tcpsocket.md) will generate a [TCPGotPort](./tcpgotport.md) event and update the value of [RemotePort](remoteport.md) accordingly.


Note that you may use *either* [RemotePort ](remoteport.md)*or* RemotePortName to identify the remote service. If you know the port number, it is normally quicker to specify [RemotePort](remoteport.md). However unless it is a *well known port number*, the use of a port name is generally more flexible. If you specify both properties, the value of RemotePortName will be ignored.


For a server [TCPSocket](./tcpsocket.md), you may not specify RemotePortName and `⎕WG` returns an empty character vector.


