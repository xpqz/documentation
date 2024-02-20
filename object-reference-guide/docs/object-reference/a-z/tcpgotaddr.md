




<h1 class="heading"><span class="name">TCPGotAddr</span></h1>

Applies To: [TCPSocket](./tcpsocket.md)


**Description**


If enabled, this event is reported when a host name (specified by the [RemoteAddrName](./remoteaddrname.md) or [LocalAddrName](./localaddrname.md) property) is resolved to an IP address.


You may not disable or nullify the operation by setting the action code for the event to `¯1` or by returning 0 from a callback function. You may also not call TCPGotAddr as a method or generate this event artificially using `⎕NQ`.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'TCPGotAddr'` or 377 |


Note that the IP address is not reported in the event message but may be obtained from [RemoteAddr](./remoteaddr.md) or [LocalAddr](./localaddr.md) as appropriate.



