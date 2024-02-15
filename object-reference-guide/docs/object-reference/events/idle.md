




<h1 class="heading"><span class="name">Idle</span></h1>
| Applies To: | [Root](../a-z/root.md) |
| --- | ---  |

| Applies To: | [Root](../a-z/root.md) | [Root](../a-z/root.md) |  |  |
| --- | --- | ---  |
| [Root](../a-z/root.md) |  |  |


Description


If enabled, this event is generated whenever APL looks to see if there is an event on the queue and finds it empty. Its purpose is to allow an application to perform some background processing when the user is not doing anything. It is unwise to use this event directly from the Session as it will occur repeatedly and may lock you out.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function is a 2-element vector as follows:

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'Idle'` or 130 |



