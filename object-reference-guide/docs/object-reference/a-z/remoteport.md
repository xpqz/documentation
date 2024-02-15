




<h1 class="heading"><span class="name">RemotePort</span></h1>
| Applies To: | [TCPSocket](./tcpsocket.md) |
| --- | ---  |

| Applies To: | [TCPSocket](./tcpsocket.md) | [TCPSocket](./tcpsocket.md) |  |  |
| --- | --- | ---  |
| [TCPSocket](./tcpsocket.md) |  |  |


Description


The RemotePort property is a scalar integer in the range 1-65536 that identifies the port number associated with a service on a remote computer.


RemotePort may only be specified by a client [TCPSocket](./tcpsocket.md) that is intended to make a connection with a server. Furthermore, it must be specified in the `⎕WC` statement that creates the [TCPSocket](./tcpsocket.md) object and it may not subsequently be changed using `⎕WS`.


Note that you may use *either* RemotePort *or* [RemotePortName](remoteportname.md) to identify the remote service. If you know the port number, it is normally quicker to specify RemotePort. However unless it is a *well known port number*, the use of a port name is generally more flexible. If you specify both properties, the value of [RemotePortName](remoteportname.md) will be ignored.


For a server [TCPSocket](./tcpsocket.md), RemotePort is determined by the port number of the connecting process and is a read-only property.



