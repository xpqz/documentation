




<h1 class="heading"><span class="name">Items</span></h1>

| Applies To: | [Combo](./combo.md) | [ComboEx](./comboex.md) | [List](./list.md) | [ListView](./listview.md) | [Spinner](./spinner.md) | [TreeView](./treeview.md) |
| --- | --- | --- | --- | --- | --- | ---  |


**Description**


This property specifies the list of items from which the user may choose.


The value of Items is a text array. It is normally specified as a vector of character vectors each of which represents an item. For a [Combo](./combo.md), [ComboEx](./comboex.md), or [List](./list.md) or [Spinner](./spinner.md), Items may also be a matrix whose rows specify items. If a character scalar or simple vector is specified, it is treated as a single item.


An empty character vector is treated the same as a vector of blanks, and represents one item.


A zero-length vector of vectors or an empty matrix represents 0 items. The default value for Items is an empty matrix.


`⎕WG 'Items'` returns an array of the same structure as was assigned by [`⎕WC`](../../Language/System%20Functions/wc.htm) or [`⎕WS`](../../Language/System%20Functions/ws.htm).



