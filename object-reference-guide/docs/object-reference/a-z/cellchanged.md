




<h1 class="heading"><span class="name">CellChanged</span></h1>

| Applies To: | [Grid](./grid.md) |
| --- | ---  |


**Description**


If enabled, this event is reported after the user has changed the contents of a cell in a [Grid](./grid.md) object and then moved to another cell or to another control outside the [Grid](./grid.md). The purpose of this event is to give the application the opportunity to perform calculations, and perhaps to update other cells in the [Grid](./grid.md) as a result of the change.


Note that this event is reported **after** the change has taken place, and after the [Values](./values.md) property has been updated. Furthermore, neither setting the event action code to `¯1` nor returning 0 from a callback function has any effect. If you wish to *validate* the new data you should use the [CellChange](./cellchange.md) (150) event instead.


The event message reported as the result of [`⎕DQ`](../../Language/System Functions/dq.htm), or supplied as the right argument to your callback function, is an 5-element vector as follows:


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'CellChanged'` or 164 |
| `[3]` | Cell row | integer |
| `[4]` | Cell column | integer |
| `[5]` | New data | number or character array |


The 5th element of the event message contains the data value that has been used to update the [Values](./values.md) property. This will be numeric if the [FieldType](./fieldtype.md) of the associated Edit object is Numeric, LongNumeric, Date, LongDate or Time. Otherwise, it will be a character array.


If you want to update an individual cell under program control, you may call [CellChange](./cellchange.md), but not CellChanged, as a method.



