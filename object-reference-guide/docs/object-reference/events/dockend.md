




<h1 class="heading"><span class="name">DockEnd</span></h1>

| Applies To: | [CoolBand](../a-z/coolband.md) | [CoolBar](../a-z/coolbar.md) | [Form](../a-z/form.md) | [SubForm](../a-z/subform.md) | [ToolControl](../a-z/toolcontrol.md) |
| --- | --- | --- | --- | --- | ---  |


**Description**


If enabled, this event is reported by a client object after it has been successfully docked in a host object.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'DockEnd'` or 484 |


This event is reported for information only and cannot be cancelled or inhibited in any way.



