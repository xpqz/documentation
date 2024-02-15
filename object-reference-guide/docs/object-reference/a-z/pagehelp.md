




<h1 class="heading"><span class="name">PageHelp</span></h1>

| Applies To: | [PropertyPage](./propertypage.md) |
| --- | ---  |


**Description**


If enabled, this event is reported when the user clicks the Help button in a Wizard [PropertySheet](./propertysheet.md). This event is reported by current [PropertyPage](./propertypage.md). The event is reported for information only and cannot be affected by a callback function.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'PageHelp'` or 352 |



