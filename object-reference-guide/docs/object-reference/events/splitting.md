




<h1 class="heading"><span class="name">Splitting</span></h1>

Applies To: [Splitter](../a-z/splitter.md)


**Description**


If enabled, this event is reported while a [Splitter](../a-z/splitter.md) object is being dragged, between a [StartSplit](../a-z/startsplit.md) and an [EndSplit](../a-z/endsplit.md). This event is only reported if full-drag is enabled.


This event is reported for information alone. You may not disable or nullify the event by setting the action code for the event to `¯1` or by returning 0 from a callback function.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 6-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'Splitting'` or 281 |
| `[3]` | Y | y-position of top left corner |
| `[4]` | X | x-position of top left corner |
| `[5]` | H | height of the Splitter |
| `[6]` | W | width of the Splitter |


See also [StartSplit](../a-z/startsplit.md), [EndSplit](../a-z/endsplit.md).



