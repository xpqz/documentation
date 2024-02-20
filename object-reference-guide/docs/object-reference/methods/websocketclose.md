




<h1 class="heading"><span class="name">WebSocketClose</span></h1>

Applies To: [HTMLRenderer](../a-z/htmlrenderer.md)


**Description**


This event is triggered when the [HTMLRenderer](../a-z/htmlrenderer.md) client closes the WebSocket.  It is for notification only.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 5-element vector as follows:


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'WebSocketClose'` or 843 |
| `[3]` | ID | Character vector containing the ID of the WebSocket |
| `[4]` | Status Code | Integer. 1000 indicates normal closure. See [https://www.iana.org/assignments/websocket/websocket.xml#close-code-number](https://www.iana.org/assignments/websocket/websocket.xml#close-code-number) . |
| `[5]` | Reason | Character vector, maximum length 123 bytes. |


When called as a method, the result is 0.

#### Example
```apl
    hr.WebSocketClose '223d0f781e95113'

```



