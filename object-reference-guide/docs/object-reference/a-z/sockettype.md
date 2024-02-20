




<h1 class="heading"><span class="name">SocketType</span></h1>

Applies To: [TCPSocket](./tcpsocket.md)


**Description**


The SocketType property is a character vector that specifies the type of the TCP/IP socket. This is either [`Stream`](../Miscellaneous/Stream Sockets.htm) (which is the default), or [`UDP`](../Miscellaneous/User Datagram Protocol UDP.htm).


SocketType must be defined when the object is created and may not be set or changed using `⎕WS`.


For two Dyalog APL applications to communicate, their [TCPSocket](./tcpsocket.md) objects must have the same SocketType.



