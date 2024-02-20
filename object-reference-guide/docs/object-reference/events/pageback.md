




<h1 class="heading"><span class="name">PageBack</span></h1>

Applies To: [PropertyPage](../a-z/propertypage.md)


**Description**


If enabled, this event is reported when the user switches from one [PropertyPage](../a-z/propertypage.md) to another in a Wizard [PropertySheet](../a-z/propertysheet.md) object by clicking its Back button. This event is reported by the old page *after* the page change has occurred and the page change may not be disabled by a callback function.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'PageBack'` or 353 |



