




<h1 class="heading"><span class="name">EnterReadOnlyCells</span></h1>

| Applies To: | [Grid](./grid.md) |
| --- | ---  |


**Description**


This is a Boolean property that specifies whether or not the user may visit read-only cells in a [Grid](./grid.md) object. Its default value is 1.


In this context, a *read-only* cell is one that satisfies one or more of the following conditions:

- it has no associated [Input](input.md) object
- its associated Input object is a [Label](./label.md)
- its associated Input object is an [Edit](./edit.md) object with [ReadOnly](readonly.md) set to 1
- its associated Input object is inactive ([Active](active.md) 0)

If EnterReadOnlyCells is set to 0 and the user clicks the mouse on a *read-only* cell, the current cell does not change although [CellDown](./celldown.md), [CellUp](./cellup.md) and [CellDblClick](./celldblclick.md) events are reported if enabled. If the user presses a cursor movement key that would otherwise cause the cursor to move into a *read-only* cell, the cursor moves instead to the nearest *editable* cell in the appropriate direction.



