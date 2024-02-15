




<h1 class="heading"><span class="name">LocalAddrName</span></h1>

| Applies To: | [TCPSocket](./tcpsocket.md) |
| --- | ---  |


**Description**


The LocalAddrName property is a character vector that specifies the host name of your computer. It may be useful when you have more than one network adapter (perhaps an Ethernet adapter and a token ring adapter) and you wish to avoid hard-coding the IP address.


Note that you may use *either* [LocalAddr](localaddr.md) *or* LocalAddrName to identify the local computer. If you specify both properties, the value of LocalAddrName will be ignored.


LocalAddrName may only be specified by a server [TCPSocket](./tcpsocket.md). Furthermore, it must be specified in the `⎕WC` statement that creates the [TCPSocket](./tcpsocket.md) object and it may not subsequently be changed using `⎕WS`.


When the specified host name has been resolved to an IP address, the [TCPSocket](./tcpsocket.md) will generate a [TCPGotAddr](./tcpgotaddr.md) event and update the value of [LocalAddr](localaddr.md) accordingly.


For a client [TCPSocket](./tcpsocket.md), you may not specify LocalAddrName and `⎕WG` returns an empty character vector.



