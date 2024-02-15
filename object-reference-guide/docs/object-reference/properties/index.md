



<h1 class="heading"><span class="name">Index</span></h1>

**Applies To**


**Description**


For a [List](../a-z/list.md) and a [Combo](../a-z/combo.md) with [Style](../a-z/style.md) `'Simple'`, this property specifies the position of the data in the list box as a positive integer value. If Index has the value "n", it means that the "nth" item in [Items](../a-z/items.md) is displayed on the top line in the list box. The value of Index is dependent upon the value of `⎕IO`. Note that Index for a [Combo](../a-z/combo.md) or [List](../a-z/list.md) cannot be set using [`⎕WC`](../../Language/System%20Functions/wc.htm). The value of Index in a [Combo](../a-z/combo.md) with a drop-down list box ([Style](../a-z/style.md) `'Drop'` or `'DropEdit'`) is always equal to `⎕IO`.


For a [Grid](../a-z/grid.md), Index is a 2-element vector that specifies the row and column number of the cell that is currently in the top left corner of the [Grid](../a-z/grid.md).


For a [TreeView](../a-z/treeview.md), Index is a positive integer value that specifies which item appears at the top of the [TreeView](../a-z/treeview.md) window.


For a [FileBox](../a-z/filebox.md), the Index property determines which of the [Filters](../a-z/filters.md) is initially selected.


For a [CoolBand](../a-z/coolband.md), the Index property specifies the position of the [CoolBand](../a-z/coolband.md) within its parent [CoolBar](../a-z/coolbar.md), relative to the other [CoolBands](../a-z/coolband.md) in the [CoolBar](../a-z/coolbar.md).


The value of Index is dependent on`⎕IO`, and its default value is equal to `⎕IO`.


