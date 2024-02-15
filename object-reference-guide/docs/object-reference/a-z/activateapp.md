




<h1 class="heading"><span class="name">ActivateApp</span></h1>
| Applies To: | [Root](./root.md) |
| --- | ---  |

| Applies To: | [Root](./root.md) | [Root](./root.md) |  |  |
| --- | --- | ---  |
| [Root](./root.md) |  |  |


Description


If enabled, this event is reported when the user switches to or from a Dyalog APL/W application.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 3-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'ActivateApp'` or 139 |
| `[3]` | Activation flag | 0 or 1 |


The Activation flag is 0 when the user switches *from* Dyalog APL to another application.


The Activation flag is  1 when the user switches *to* Dyalog APL from another application.



