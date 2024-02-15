




<h1 class="heading"><span class="name">EnterReadOnlyCells</span></h1>

| Applies To: | [Grid](../a-z/grid.md) |
| --- | ---  |


**Description**


This is a Boolean property that specifies whether or not the user may visit read-only cells in a [Grid](../a-z/grid.md) object. Its default value is 1.


In this context, a *read-only* cell is one that satisfies one or more of the following conditions:

- it has no associated [Input](../a-z/input.md) object
- its associated Input object is a [Label](../a-z/label.md)
- its associated Input object is an [Edit](../a-z/edit.md) object with [ReadOnly](../a-z/readonly.md) set to 1
- its associated Input object is inactive ([Active](../a-z/active.md) 0)

If EnterReadOnlyCells is set to 0 and the user clicks the mouse on a *read-only* cell, the current cell does not change although [CellDown](../a-z/celldown.md), [CellUp](../a-z/cellup.md) and [CellDblClick](../a-z/celldblclick.md) events are reported if enabled. If the user presses a cursor movement key that would otherwise cause the cursor to move into a *read-only* cell, the cursor moves instead to the nearest *editable* cell in the appropriate direction.



