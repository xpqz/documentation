




<h1 class="heading"><span class="name">PageCancel</span></h1>

| Applies To: | [PropertyPage](./propertypage.md) |
| --- | ---  |


**Description**


If enabled, this event is reported when the user presses the Cancel button in a [PropertySheet](./propertysheet.md) object and is reported by the current [PropertyPage](./propertypage.md). This event is reported for information only and may not be disabled by a callback function. However, the operation will also generate a Close event reported by the [PropertySheet](./propertysheet.md) itself that may be disabled by a callback.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'PageCancel'` or 351 |



