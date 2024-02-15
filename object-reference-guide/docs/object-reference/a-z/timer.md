




<h1 class="heading"><span class="name">Timer</span></h1>

| Applies To: | [Timer](./timer.md) |
| --- | ---  |


**Description**


This event is generated at regular intervals by a [Timer](./timer.md) object and is typically used to fire a callback function to perform a task repeatedly. Returning a 0 from a callback function attached to a Timer event has no effect. The event message reported as the result of [`⎕DQ`](../../Language/System%20Functions/dq.htm), or supplied as the right argument to your callback function, is a 2 element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'Timer'` or 140 |



