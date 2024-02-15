




<h1 class="heading"><span class="name">WinIniChange</span></h1>
| Applies To: | [Root](./root.md) |
| --- | ---  |

| Applies To: | [Root](./root.md) | [Root](./root.md) |  |  |
| --- | --- | ---  |
| [Root](./root.md) |  |  |


Description


If enabled, this event is reported when another application changes relevant registry settings using the standard API calls. The event is reported after the change has taken place and cannot be disabled or inhibited in any way. If your application depends upon registry settings, this event gives you the opportunity of refreshing these parameters if they are changed.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'WinIniChange'` or 133 |



