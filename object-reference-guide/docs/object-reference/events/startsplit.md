




<h1 class="heading"><span class="name">StartSplit</span></h1>

| Applies To: | [Splitter](../a-z/splitter.md) |
| --- | ---  |


**Description**


If enabled, this event is reported when the user depresses the left mouse button over a [Splitter](../a-z/splitter.md) object to signify the beginning of a drag operation.


This event is reported for information alone. You may not disable or nullify the event by setting the action code for the event to `¯1` or by returning 0 from a callback function.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'StartSplit'` or 280 |


See also [EndSplit](../a-z/endsplit.md), [Splitting](../a-z/splitting.md).



