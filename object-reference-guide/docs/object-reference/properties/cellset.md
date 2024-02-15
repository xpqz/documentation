




<h1 class="heading"><span class="name">CellSet</span></h1>
| Applies To: | [Grid](../a-z/grid.md) |
| --- | ---  |

| Applies To: | [Grid](../a-z/grid.md) | [Grid](../a-z/grid.md) |  |  |
| --- | --- | ---  |
| [Grid](../a-z/grid.md) |  |  |


Description


This property identifies which cells in a [Grid](../a-z/grid.md) are *set* (i.e. have values) and which are empty. Its purpose is to allow large numeric matrices containing blank cells to be displayed and edited efficiently.


The CellSet property is a Boolean matrix with the same shape as the [Values](../a-z/values.md) property. If an element of CellSet is 0, the cell is defined to be empty. Empty cells are displayed as blank and the cell contents by the [Values](../a-z/values.md) property are ignored.


A more direct way to handle empty cells is to set  the corresponding elements of [Values](../a-z/values.md) to empty vectors. However, if [Values](../a-z/values.md) is otherwise entirely numeric, this makes the array nested when it would otherwise be simple. For large numeric matrices, this penalty can be severe. For example, a 100x100 array of 2-byte integer values occupies about 20Kb of workspace. Setting one or more elements of the array to an empty vector increases its size to 200Kb. However, because it is Boolean, the size of the CellSet property for a 100x100 array is only 1.27Kb and represents a significant space saving.


Note that if the [Values](../a-z/values.md) property contains text and is therefore nested anyway, the CellSet property is not helpful in conserving workspace, although it may still be useful to separate empty cells from real data.


You can dynamically change a single element of CellSet using the [SetCellSet](../a-z/setcellset.md) method.



