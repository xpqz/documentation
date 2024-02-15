




<h1 class="heading"><span class="name">RemoteAddrName</span></h1>
| Applies To: | [TCPSocket](../a-z/tcpsocket.md) |
| --- | ---  |

| Applies To: | [TCPSocket](../a-z/tcpsocket.md) | [TCPSocket](../a-z/tcpsocket.md) |  |  |
| --- | --- | ---  |
| [TCPSocket](../a-z/tcpsocket.md) |  |  |


Description


The RemoteAddrName property is a character vector that specifies the host name of the remote computer to which you wish to make a connection.


RemoteAddrName may only be specified by a client [TCPSocket](../a-z/tcpsocket.md) that is intended to make a connection with a server. Furthermore, it must be specified in the `⎕WC` statement that creates the [TCPSocket](../a-z/tcpsocket.md) object and it may not subsequently be changed using `⎕WS`.


When the specified host name has been resolved to an IP address, the [TCPSocket](../a-z/tcpsocket.md) will generate a [TCPGotAddr](../a-z/tcpgotaddr.md) event and update the value of [RemoteAddr](../a-z/remoteaddr.md) accordingly.


Note that you may use *either* [RemoteAddr ](../a-z/remoteaddr.md)*or* RemoteAddrName to identify the remote computer. If you know its IP address, it is normally quicker to specify [RemoteAddr](../a-z/remoteaddr.md). If you specify both properties, the value of RemoteAddrName will be ignored.


For a server [TCPSocket](../a-z/tcpsocket.md), you may not specify RemoteAddrName and `⎕WG` returns an empty character vector.



