




<h1 class="heading"><span class="name">PageDeactivate</span></h1>

Applies To: [PropertyPage](../a-z/propertypage.md)


**Description**


If enabled, this event is reported when the user switches from one [PropertyPage](../a-z/propertypage.md) to another in a [PropertySheet](../a-z/propertysheet.md) object. This event is reported by the old page *after* the page change has occurred and the page change may not be disabled by a callback function.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'PageDeactivate'` or 361 |



