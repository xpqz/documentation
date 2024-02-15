




<h1 class="heading"><span class="name">SelItems</span></h1>

| Applies To: | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [Grid](../a-z/grid.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [TreeView](../a-z/treeview.md) |
| --- | --- | --- | --- | --- | --- | ---  |


**Description**


This property determines which (if any) of the items in an object are currently selected and highlighted. Except in a Grid, it is a Boolean vector with one element per item in the list. A value of 1 means "selected"; 0 means "not selected".


This property is used after a [Select](../a-z/select.md) event to identify which item has been chosen. In a [Combo](../a-z/combo.md) or a [List](../a-z/list.md) with [Style](../a-z/style.md) `'Single'` it will contain only a single 1.


SelItems should also be used to pre-set the contents of the edit field in a [Combo](../a-z/combo.md) box with [Style](../a-z/style.md) `'Drop'`. In [Combo](../a-z/combo.md) boxes with [Style](../a-z/style.md) `'Simple'` or `'DropEdit'`, the contents of the edit field may also be specified by the [Text](../a-z/text.md) property. If you specify both, the value of [Text](../a-z/text.md) takes precedence.


In a [Grid,](../a-z/grid.md) SelItems is a 2-element integer vector. The first element identifies the row and column coordinates respectively of the first cell(s) in the selected block(s) and the second, the row and column coordinates of the last cell(s) in the selected block(s). If the [CellSelect](../a-z/cellselect.md) property allows only a single block of cells to be selected, each set of coordinates is a 2-element vector. If the [CellSelect](../a-z/cellselect.md) property permits more than one block of cells to be selected, each set of coordinates is a 2-column matrix with one row per selected block, whose columns identify the first row and column, and the last row and column respectively of each selected block.



