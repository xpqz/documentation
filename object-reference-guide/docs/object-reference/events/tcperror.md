




<h1 class="heading"><span class="name">TCPError</span></h1>
| Applies To: | [TCPSocket](../a-z/tcpsocket.md) |
| --- | ---  |

| Applies To: | [TCPSocket](../a-z/tcpsocket.md) | [TCPSocket](../a-z/tcpsocket.md) |  |  |
| --- | --- | ---  |
| [TCPSocket](../a-z/tcpsocket.md) |  |  |


Description


This event is generated when a fatal TCP/IP error occurs and is reported by a [TCPSocket](../a-z/tcpsocket.md) object.


The default processing for this event is to display a message box containing details of the TCP/IP error. You may disable the display of this message box by setting the action code for the event to `¯1` or by returning 0 from a callback function attached to it.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 3-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'TCPError'` or 370 |
| `[3]` | Error code | a number |
| `[4]` | Error text | a character vector |



