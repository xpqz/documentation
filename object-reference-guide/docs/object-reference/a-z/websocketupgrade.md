




<h1 class="heading"><span class="name">WebSocketUpgrade</span></h1>
| Applies To: | [HTMLRenderer](./htmlrenderer.md) |
| --- | ---  |

| Applies To: | [HTMLRenderer](./htmlrenderer.md) | [HTMLRenderer](./htmlrenderer.md) |  |  |
| --- | --- | ---  |
| [HTMLRenderer](./htmlrenderer.md) |  |  |


Description


This event is reported when the client component of an [HTMLRenderer](./htmlrenderer.md) object opens a WebSocket and the requested URL matches a pattern specified by the [InterceptedURLs](./interceptedurls.md) property. If there is no match, the connection request is processed as an external request by the [Chromium Embedded Framework (CEF) https://en.wikipedia.org/wiki/Chromium_Embedded_Framework.](https://en.wikipedia.org/wiki/Chromium_Embedded_Framework)




The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 6-element vector as follows:

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'WebSocketUpgrade'` or 841 |
| `[3]` | ID | Character vector containing the ID of the WebSocket |
| `[4]` | URL | The requested URL of the WebSocket |
| `[5]` | Headers | ASCII including CRLF |
| `[6]` | Type | Character vector `'auto'` or `'manual'` |



The protocol for establishing the connection is defined by [InterceptedURLs](./interceptedurls.md) and is reported by the 6th element (Type) of the event message.


If Type is `'auto'`, the protocol is handled internally and this event is reported when the connection has already been made. Should the connection fail, a [WebSocketError](websocketerror.md) event will be reported instead.


If Type is `'manual'`, a callback function for WebSocketUpgrade is mandatory and is responsible for completing (or denying) the connection. This is achieved by setting the 5th element of the event message (Headers) to indicate an appropriate positive or negative response to the requesthttps://tools.ietf.org/html/rfc6455#section-1.3 and returning the entire event message as its result. If a valid response is not generated in this way, the connection will time-out causing a [WebSocketError](websocketerror.md) event. For further information, see [https://tools.ietf.org/html/rfc6455#section-1.3](https://tools.ietf.org/html/rfc6455#section-1.3).


In both cases,  the WebSocket ID is subsequently required to send a message  by calling the [WebSocketSend](websocketsend.md) method or to close the connection using the   [WebSocketClose](websocketclose.md) method.


Note that several WebSocket connections may be made concurrently.

#### Example
```apl
┌→────────────────────────────────────────────────────────┐
│      ┌→───────────────┐ ┌→──────────────┐ ┌→──────────┐ │
│ #.hr │WebSocketUpgrade│ │5d61d8330065608│ │ws://myapp/│ │
│      └────────────────┘ └───────────────┘ └───────────┘ │
└∊────────────────────────────────────────────────────────┘

```


