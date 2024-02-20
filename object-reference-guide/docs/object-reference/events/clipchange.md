




<h1 class="heading"><span class="name">ClipChange</span></h1>

Applies To: [Clipboard](../a-z/clipboard.md)


**Description**


If enabled, this event is reported when another application changes the contents of the Windows clipboard.


The event message reported as the result of [`⎕DQ`](../../Language/System Functions/dq.htm), or supplied as the right argument to your callback function, is a 2-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'ClipChange'` or 120 |



