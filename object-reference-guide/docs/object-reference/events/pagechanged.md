




<h1 class="heading"><span class="name">PageChanged</span></h1>
| Applies To: | [PropertyPage](../a-z/propertypage.md) |
| --- | ---  |

| Applies To: | [PropertyPage](../a-z/propertypage.md) | [PropertyPage](../a-z/propertypage.md) |  |  |
| --- | --- | ---  |
| [PropertyPage](../a-z/propertypage.md) |  |  |


Description


If enabled, this event is reported when the [Changed](../a-z/changed.md) property of a [PropertyPage](../a-z/propertypage.md) is altered by user action. It is *not* reported if you reset the [Changed](../a-z/changed.md) property using `⎕WS`.


The [Changed](../a-z/changed.md) property is reset by two separate user actions. It is set to 1 when the user alters any of the controls on the [PropertyPage](../a-z/propertypage.md). It is reset to 0 when the user clicks the Apply button, although this action may be disabled by a callback function on the [PageApply](../a-z/pageapply.md) event.


The PageChanged event is reported for information only and may not itself be disabled or affected by a callback function.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 3-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'PageChanged'` or 356 |
| `[3]` | Changed value | New value for the [Changed](../a-z/changed.md) property (0 or 1). |



