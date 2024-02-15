




<h1 class="heading"><span class="name">TCPSocket</span></h1>

| [Parents](../ParentLists/TCPSocket.htm) | [Children](../ChildLists/TCPSocket.htm) | [Properties](../PropLists/TCPSocket.htm) | [Methods](../MethodLists/TCPSocket.htm) | [Events](../EventLists/TCPSocket.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | The TCPSocket object provides an interface to TCP/IP. |
| --- | ---  |


**Description**


The TCPSocket object provides an event-driven mechanism to communicate with
other programs (including Dyalog APL) via TCP sockets. Dyalog recommends that Conga is used in preference to TCPSockets in new applications.



The [SocketType](./sockettype.md) property is a
character vector that specifies the type of the TCP/IP socket. This is either '`Stream'` (the
default), or `'UDP'`. [SocketType](./sockettype.md) must be defined when the object is created and cannot be set or changed using `⎕WS`.


The Style property is a character vector that specifies the type of data
transmitted or received by the socket; it may be `'Char'`,
`'Raw'`, or `'APL'`.
The value `'APL'` is valid only if the [SocketType](./sockettype.md) is '`Stream'`.


The [Encoding](./encoding.md) property is a character
vector that specifies how character data are encoded or translated. The possible
values are `'None'`, `'UTF-8'`, `'Classic'`
or `'Unicode'`, depending upon the value of the Style
property.


[LocalAddr](./localaddr.md) and [LocalPort](./localport.md) properties identify your end of the connection; [RemoteAddr](./remoteaddr.md) and [RemotePort](./remoteport.md) identify the other end of
the connection. The values of the two sets of properties are clearly
symmetrical; your [LocalAddr](./localaddr.md) is your
partner's [RemoteAddr](./remoteaddr.md), and there are
strict rules concerning which of them you and your partner may set. See the
individual descriptions of these properties for details.


The [SocketNumber](./socketnumber.md) property is the
Window handle of the socket attached to the TCPSocket object and is generally a
read-only property. The only time that [SocketNumber](./socketnumber.md) may be specified is when a server replicates (clones) a listening socket to
which a client has just connected.


