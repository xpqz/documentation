




<h1 class="heading"><span class="name">AddCol</span></h1>

| Applies To: | [Grid](../a-z/grid.md) |
| --- | ---  |


**Description**


If enabled, this event is reported by the [Grid](../a-z/grid.md) object if the user presses the Cursor Right key, and the current cell ([CurCell](../a-z/curcell.md)) is within the last column on the [Grid](../a-z/grid.md). The default action is to append a new column to the contents of the [Grid](../a-z/grid.md). If you attach a callback function to this event and have it return a value of 0, a new column will not be appended to the [Grid](../a-z/grid.md). Note that the event will not be generated unless the second element of the [AutoExpand](../a-z/autoexpand.md) property is set to 1.




The event message reported as the result of [`⎕DQ`](../../Language/System Functions/dq.htm), or supplied as the right argument to your callback function, is a 3-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'AddCol'` or 153 |
| `[3]` | Column number | number of the new column (integer) |




An application may insert a new column into a [Grid](../a-z/grid.md) by calling 
      AddCol as a method. The argument is a 1 to 7-element array as 
      follows:


| `[1]` | Column number | number of the new column (integer) |
| --- | --- | ---  |
| `[2]` | Column title | character vector or matrix |
| `[3]` | Column width | integer |
| `[4]` | Undo flag | 0 or 1 |
| `[5]` | Resize flag | 0 or 1 |
| `[6]` | Title colour | negative integer or 3-element RGB vector |
| `[7]` | Line type | integer |



If you are using default column headings, *Column title* will be ignored and the columns will be re-labelled with the default titles. If you have set [ColTitles](../a-z/coltitles.md), the title you specify will be inserted. If you omit *Column title*, a blank title will be inserted.


Similarly, if you have not previously set [CellWidths](../a-z/cellwidths.md), [ResizeCols](../a-z/resizecols.md), [ColTitleFCol](../a-z/coltitlefcol.md) or [ColLineTypes](../a-z/collinetypes.md), or if you have given them a scalar value, the corresponding parameter will be ignored. However, if you have specified [CellWidths](../a-z/cellwidths.md), [ResizeCols](../a-z/resizecols.md), [ColTitleFCol](../a-z/coltitlefcol.md) or [ColLineTypes](../a-z/collinetypes.md) to be a *vector*, the number you specify in the corresponding parameter will be inserted into the appropriate property vector.


If you omit to specify *Column width* for the new column, it will be assigned a default value; new values for the other properties default to 0.


*Undo flag* (default 1) specifies whether or not the addition of the new column may subsequently be undone by an [Undo](../a-z/undo.md) event.


To insert a new column before the first one, you must specify the *Column number* as 1 (or 0 if `⎕IO` is 0). To add a new column after the last one, you may specify any number greater than the current number of columns. The data in the new column will be set to 0 if the [Values](../a-z/values.md) property is numeric, or to an empty character vector otherwise.


