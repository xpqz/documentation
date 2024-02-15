




<h1 class="heading"><span class="name">PageApply</span></h1>

| Applies To: | [PropertyPage](../a-z/propertypage.md) |
| --- | ---  |


**Description**


If enabled, this event is reported when the user clicks the Apply button in a [PropertySheet](../a-z/propertysheet.md). Note however, that the event is actually reported by each of its [PropertyPage](../a-z/propertypage.md) objects whose Changed property is currently 1, i.e. the event is reported by each of the pages that the user has changed.


The default processing for this event is to set the Changed property of the [PropertyPage](../a-z/propertypage.md) to 0. If you disable the event or return a 0 from a callback function, the Changed property is not reset. Note that the Apply button in a [PropertySheet](../a-z/propertysheet.md) is active if the value of the Changed property of *any* of the [PropertyPage](../a-z/propertypage.md) objects is 1.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'PageApply'` or 350 |



