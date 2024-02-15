




<h1 class="heading"><span class="name">TCPSocket</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | The TCPSocket object provides an interface to TCP/IP. |
| --- | --- | ---  |
| Parents | [Detach](../a-z/detach.md) [TCPSend](../a-z/tcpsend.md) [TCPGetHostID](../a-z/tcpgethostid.md) [TCPSendPicture](../a-z/tcpsendpicture.md) [Wait](../a-z/wait.md) | [Detach](../a-z/detach.md) | [TCPSend](../a-z/tcpsend.md) | [TCPGetHostID](../a-z/tcpgethostid.md) | [TCPSendPicture](../a-z/tcpsendpicture.md) | [Wait](../a-z/wait.md) |  |
| [Detach](../a-z/detach.md) | [TCPSend](../a-z/tcpsend.md) | [TCPGetHostID](../a-z/tcpgethostid.md) |
| [TCPSendPicture](../a-z/tcpsendpicture.md) | [Wait](../a-z/wait.md) |  |
| Children | [Detach](../a-z/detach.md) [TCPSend](../a-z/tcpsend.md) [TCPGetHostID](../a-z/tcpgethostid.md) [TCPSendPicture](../a-z/tcpsendpicture.md) [Wait](../a-z/wait.md) | [Detach](../a-z/detach.md) | [TCPSend](../a-z/tcpsend.md) | [TCPGetHostID](../a-z/tcpgethostid.md) | [TCPSendPicture](../a-z/tcpsendpicture.md) | [Wait](../a-z/wait.md) |  |
| [Detach](../a-z/detach.md) | [TCPSend](../a-z/tcpsend.md) | [TCPGetHostID](../a-z/tcpgethostid.md) |
| [TCPSendPicture](../a-z/tcpsendpicture.md) | [Wait](../a-z/wait.md) |  |
| Properties | [Detach](../a-z/detach.md) [TCPSend](../a-z/tcpsend.md) [TCPGetHostID](../a-z/tcpgethostid.md) [TCPSendPicture](../a-z/tcpsendpicture.md) [Wait](../a-z/wait.md) | [Detach](../a-z/detach.md) | [TCPSend](../a-z/tcpsend.md) | [TCPGetHostID](../a-z/tcpgethostid.md) | [TCPSendPicture](../a-z/tcpsendpicture.md) | [Wait](../a-z/wait.md) |  |
| [Detach](../a-z/detach.md) | [TCPSend](../a-z/tcpsend.md) | [TCPGetHostID](../a-z/tcpgethostid.md) |
| [TCPSendPicture](../a-z/tcpsendpicture.md) | [Wait](../a-z/wait.md) |  |
| Methods | [Detach](../a-z/detach.md) [TCPSend](../a-z/tcpsend.md) [TCPGetHostID](../a-z/tcpgethostid.md) [TCPSendPicture](../a-z/tcpsendpicture.md) [Wait](../a-z/wait.md) | [Detach](../a-z/detach.md) | [TCPSend](../a-z/tcpsend.md) | [TCPGetHostID](../a-z/tcpgethostid.md) | [TCPSendPicture](../a-z/tcpsendpicture.md) | [Wait](../a-z/wait.md) |  |
| [Detach](../a-z/detach.md) | [TCPSend](../a-z/tcpsend.md) | [TCPGetHostID](../a-z/tcpgethostid.md) |
| [TCPSendPicture](../a-z/tcpsendpicture.md) | [Wait](../a-z/wait.md) |  |
| Events | [Detach](../a-z/detach.md) [TCPSend](../a-z/tcpsend.md) [TCPGetHostID](../a-z/tcpgethostid.md) [TCPSendPicture](../a-z/tcpsendpicture.md) [Wait](../a-z/wait.md) | [Detach](../a-z/detach.md) | [TCPSend](../a-z/tcpsend.md) | [TCPGetHostID](../a-z/tcpgethostid.md) | [TCPSendPicture](../a-z/tcpsendpicture.md) | [Wait](../a-z/wait.md) |  |
| [Detach](../a-z/detach.md) | [TCPSend](../a-z/tcpsend.md) | [TCPGetHostID](../a-z/tcpgethostid.md) |
| [TCPSendPicture](../a-z/tcpsendpicture.md) | [Wait](../a-z/wait.md) |  |


Description


The TCPSocket object provides an event-driven mechanism to communicate with
other programs (including Dyalog APL) via TCP sockets. Dyalog recommends that Conga is used in preference to TCPSockets in new applications.



The [SocketType](../a-z/sockettype.md) property is a
character vector that specifies the type of the TCP/IP socket. This is either '`Stream'` (the
default), or `'UDP'`. [SocketType](../a-z/sockettype.md) must be defined when the object is created and cannot be set or changed using `⎕WS`.


The Style property is a character vector that specifies the type of data
transmitted or received by the socket; it may be `'Char'`,
`'Raw'`, or `'APL'`.
The value `'APL'` is valid only if the [SocketType](../a-z/sockettype.md) is '`Stream'`.


The [Encoding](../a-z/encoding.md) property is a character
vector that specifies how character data are encoded or translated. The possible
values are `'None'`, `'UTF-8'`, `'Classic'`
or `'Unicode'`, depending upon the value of the Style
property.


[LocalAddr](../a-z/localaddr.md) and [LocalPort](../a-z/localport.md) properties identify your end of the connection; [RemoteAddr](../a-z/remoteaddr.md) and [RemotePort](../a-z/remoteport.md) identify the other end of
the connection. The values of the two sets of properties are clearly
symmetrical; your [LocalAddr](../a-z/localaddr.md) is your
partner's [RemoteAddr](../a-z/remoteaddr.md), and there are
strict rules concerning which of them you and your partner may set. See the
individual descriptions of these properties for details.


The [SocketNumber](../a-z/socketnumber.md) property is the
Window handle of the socket attached to the TCPSocket object and is generally a
read-only property. The only time that [SocketNumber](../a-z/socketnumber.md) may be specified is when a server replicates (clones) a listening socket to
which a client has just connected.


