




<h1 class="heading"><span class="name">DuplicateColumn</span></h1>
| Applies To: | [Grid](../a-z/grid.md) |
| --- | ---  |

| Applies To: | [Grid](../a-z/grid.md) | [Grid](../a-z/grid.md) |  |  |
| --- | --- | ---  |
| [Grid](../a-z/grid.md) |  |  |


Description


This method is used to duplicate a column in a [Grid](../a-z/grid.md) object.


The argument to DuplicateColumn is a 2, 3, 4 or 5-element vector as follows:

| `[1]` | Source Column number | number of the column (integer) to be duplicated |
| --- | --- | ---  |
| `[2]` | Target Column number | new column number (integer) |
| `[3]` | Comment flag | 0 or 1 (optional, default 1) |
| `[4]` | Lock flag | 0 or 1 (optional, default 1) |
| `[5]` | Undo flag | 0 or 1 (optional; default 0) |


If the *Comment flag* is 1 (the default), any Comments associated with cells in the source column are duplicated in the target column.


If the *Lock flag* is 1 (the default), the lock state of the column is duplicated; otherwise, the new column is not locked.


If the *Undo flag* is 1, the column may subsequently be restored by invoking the Undo method. If this element is omitted or is 0, the operation may not be undone.



