




<h1 class="heading"><span class="name">DelCol</span></h1>

| Applies To: | [Grid](./grid.md) |
| --- | ---  |


**Description**


This method is used to delete a specified column from a [Grid](./grid.md) object.


The argument to DelCol is a 1 or 2-element vector as follows:


| `[1]` | Column number | number of the column (integer) to delete |
| --- | --- | ---  |
| `[2]` | Undo flag | 0 or 1 (optional; default 0) |


If the *Undo flag* 1, the column may subsequently be restored by invoking the [Undo](./undo.md) method. If the *Undo flag* is omitted or is 0, the operation may not be undone.



