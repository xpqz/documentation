




<h1 class="heading"><span class="name">RemoteAddrName</span></h1>
| Applies To: | [TCPSocket](./tcpsocket.md) |
| --- | ---  |

| Applies To: | [TCPSocket](./tcpsocket.md) | [TCPSocket](./tcpsocket.md) |  |  |
| --- | --- | ---  |
| [TCPSocket](./tcpsocket.md) |  |  |


Description


The RemoteAddrName property is a character vector that specifies the host name of the remote computer to which you wish to make a connection.


RemoteAddrName may only be specified by a client [TCPSocket](./tcpsocket.md) that is intended to make a connection with a server. Furthermore, it must be specified in the `⎕WC` statement that creates the [TCPSocket](./tcpsocket.md) object and it may not subsequently be changed using `⎕WS`.


When the specified host name has been resolved to an IP address, the [TCPSocket](./tcpsocket.md) will generate a [TCPGotAddr](./tcpgotaddr.md) event and update the value of RemoteAddr accordingly.


Note that you may use *either* RemoteAddr *or* RemoteAddrName to identify the remote computer. If you know its IP address, it is normally quicker to specify RemoteAddr. If you specify both properties, the value of RemoteAddrName will be ignored.


For a server [TCPSocket](./tcpsocket.md), you may not specify RemoteAddrName and `⎕WG` returns an empty character vector.



