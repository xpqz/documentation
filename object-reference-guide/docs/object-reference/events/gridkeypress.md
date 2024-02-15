



<h1 class="heading"><span class="name">GridKeyPress</span></h1>

| Applies To: | [Grid](../a-z/grid.md) |
| --- | ---  |


**Description**


If enabled, this event is generated when the user presses and releases a key in a [Grid](../a-z/grid.md) cell.


The GridKeyPress is reported on the [Grid](../a-z/grid.md), *after* the [KeyPress](../a-z/keypress.md) event, which is reported on the [Input](../a-z/input.md) object associated with the current cell.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 6-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'GridKeyPress'` or 24 |
| `[3]` | Input Code | character scalar or vector |
| `[4]` | ASCII code | integer scalar |
| `[5]` | Key Number | integer scalar |
| `[6]` | Shift State | integer scalar |
| `[7]` | Input Object | ref or character vector |


For a full description of elements [3-6], see [KeyPress](../a-z/keypress.md) event.


The 7th element of the event message contains either a reference to, or the name of the Input object associated with the current cell and on which the corresponding [KeyPress](../a-z/keypress.md) event has been reported.


The default action of the GridKeyPress event is to pass a [KeyPress](../a-z/keypress.md) event message back to the appropriate Input object to be actioned. The GridKeyPress is reported on the Grid, after the [KeyPress](../a-z/keypress.md) event on the Input object. If a callback on the Input object's [KeyPress](../a-z/keypress.md) event returns 0 or if a callback on GridKeyPress returns 0, the keystroke will be ignored.


