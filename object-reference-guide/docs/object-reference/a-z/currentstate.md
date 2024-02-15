




<h1 class="heading"><span class="name">CurrentState</span></h1>

| Applies To: | [TCPSocket](./tcpsocket.md) |
| --- | ---  |


**Description**


The CurrentState property is a read-only property that reports the current state of a [TCPSocket](./tcpsocket.md) object. Its possible values and their means are as follows:


| CurrentState | Description |
| --- | ---  |
| `'Open'` | a client socket that is not yet connected or a UDP socket |
| `'Bound'` | a server socket that has been bound |
| `'Listening'` | a server socket to which a client has not yet connected |
| `'Connected'` | a client or server socket that is connected |
| `'IHaveClosed'` | a temporary state on the way to Closed |
| `'PartnerHasClosed'` | a temporary state on the way to Closed |
| `'Closed'` | a socket that has been closed by both client and server |




