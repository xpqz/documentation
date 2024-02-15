




<h1 class="heading"><span class="name">LocalPortName</span></h1>
| Applies To: | [TCPSocket](./tcpsocket.md) |
| --- | ---  |

| Applies To: | [TCPSocket](./tcpsocket.md) | [TCPSocket](./tcpsocket.md) |  |  |
| --- | --- | ---  |
| [TCPSocket](./tcpsocket.md) |  |  |


Description


The LocalPortName property is a character vector that specifies the port name of the local service that you wish to offer as a server.


Note that you may use *either* LocalPort *or* LocalPortName to identify the service. The use of LocalPortName is slightly slower but it avoids hard-coding the port number in your program and is generally more flexible. If you specify both properties, the value of LocalPortName will be ignored.


LocalPortName may be specified only by the process that is initiating the connection (the server) and must be set by the `⎕WC` statement that creates the [TCPSocket](./tcpsocket.md). LocalPortName may not subsequently be changed using `⎕WS`.


When the specified port name has been resolved to a port number, the [TCPSocket](./tcpsocket.md) will generate a [TCPGotPort](./tcpgotport.md) event and update the value of LocalPort accordingly.


For a client [TCPSocket](./tcpsocket.md), you may not specify LocalPortName and `⎕WG` returns an empty character vector.



