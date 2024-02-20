



<h1 class="heading"><span class="name">Index</span></h1>

**Applies To**


**Description**


For a [List](./list.md) and a [Combo](./combo.md) with [Style](style.md) `'Simple'`, this property specifies the position of the data in the list box as a positive integer value. If Index has the value "n", it means that the "nth" item in [Items](items.md) is displayed on the top line in the list box. The value of Index is dependent upon the value of `⎕IO`. Note that Index for a [Combo](./combo.md) or [List](./list.md) cannot be set using [`⎕WC`](../../Language/System Functions/wc.htm). The value of Index in a [Combo](./combo.md) with a drop-down list box ([Style](style.md) `'Drop'` or `'DropEdit'`) is always equal to `⎕IO`.


For a [Grid](./grid.md), Index is a 2-element vector that specifies the row and column number of the cell that is currently in the top left corner of the [Grid](./grid.md).


For a [TreeView](./treeview.md), Index is a positive integer value that specifies which item appears at the top of the [TreeView](./treeview.md) window.


For a [FileBox](./filebox.md), the Index property determines which of the [Filters](filters.md) is initially selected.


For a [CoolBand](./coolband.md), the Index property specifies the position of the [CoolBand](./coolband.md) within its parent [CoolBar](./coolbar.md), relative to the other [CoolBands](./coolband.md) in the [CoolBar](./coolbar.md).


The value of Index is dependent on`⎕IO`, and its default value is equal to `⎕IO`.


