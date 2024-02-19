



<h1 class="heading"><span class="name">AutoExpand</span></h1>

| Applies To: | [Grid](./grid.md) |
| --- | ---  |


**Description**


This property is a 2-element Boolean value that specifies whether or not rows and columns may be added to a [Grid](./grid.md) object by the user.


If the first element of AutoExpand is 1, a row is added when the current cell is within the last row of the [Grid](./grid.md) and the user presses Cursor Down


Similarly, if the second element is 1, a column is added when the current cell is within the last column of the [Grid](./grid.md) and the user presses Cursor Right.


Note that when a row or column is added, the appropriate properties (including [Values](values.md) and [CellTypes](CellTypes.htm)) are expanded accordingly.


The default value for AutoExpand is (0 0).


If AutoExpand is enabled, the [Grid](./grid.md) generates [AddRow](./addrow.md) and [AddCol](./addcol.md) events. You can return a zero from a callback function to selectively prevent the addition of rows and columns if appropriate.


