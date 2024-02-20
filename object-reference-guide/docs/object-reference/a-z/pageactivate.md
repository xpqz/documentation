




<h1 class="heading"><span class="name">PageActivate</span></h1>

Applies To: [PropertyPage](./propertypage.md)


**Description**


If enabled, this event is reported when the user switches from one [PropertyPage](./propertypage.md) to another in a [PropertySheet](./propertysheet.md) object. This event is reported by the new page *after* the page change has occurred and the page change may not be disabled by a callback function.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'PageActivate'` or 360 |


You may select a particular page by calling PageActivate as a method, or by setting the [PageActive](./pageactive.md) or [PageActiveObject](./pageactiveobject.md) property of the [PropertySheet](./propertysheet.md).



