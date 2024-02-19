




<h1 class="heading"><span class="name">Items</span></h1>

| Applies To: | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [Spinner](../a-z/spinner.md) | [TreeView](../a-z/treeview.md) |
| --- | --- | --- | --- | --- | --- | ---  |


**Description**


This property specifies the list of items from which the user may choose.


The value of Items is a text array. It is normally specified as a vector of character vectors each of which represents an item. For a [Combo](../a-z/combo.md), [ComboEx](../a-z/comboex.md), or [List](../a-z/list.md) or [Spinner](../a-z/spinner.md), Items may also be a matrix whose rows specify items. If a character scalar or simple vector is specified, it is treated as a single item.


An empty character vector is treated the same as a vector of blanks, and represents one item.


A zero-length vector of vectors or an empty matrix represents 0 items. The default value for Items is an empty matrix.


`⎕WG 'Items'` returns an array of the same structure as was assigned by [`⎕WC`](../../Language/System Functions/wc.htm) or [`⎕WS`](../../Language/System Functions/ws.htm).



