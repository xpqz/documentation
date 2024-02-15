




<h1 class="heading"><span class="name">RowTreeDepth</span></h1>
| Applies To: | [Grid](./grid.md) |
| --- | ---  |

| Applies To: | [Grid](./grid.md) | [Grid](./grid.md) |  |  |
| --- | --- | ---  |
| [Grid](./grid.md) |  |  |


Description


The RowTreeDepth property specifies the structure of the rows in a [Grid](./grid.md) object. It is either a scalar 0 or an integer vector of the same length as the number of rows in the [Grid](./grid.md). RowTreeDepth is similar to the [Depth](depth.md) property of the [TreeView](./treeview.md) object.


A value of 0 indicates that the corresponding row is a top-level row. A value of 1 indicates that the corresponding row is a child of the most recent row whose RowTreeDepth is 0; a value of 2 indicates that the corresponding row is a child of the most recent row whose RowTreeDepth is 1, and so forth.


When you set RowTreeDepth, the [Grid](./grid.md) is redrawn so that only rows with a RowTreeDepth of 0 are visible.


The [RowSetVisibleDepth](./rowsetvisibledepth.md) method can be used to make data visible to a specific depth.

#### Example:
```apl
      'F'⎕WC'Form' 'Grid: TreeView Feature'
      'F.G'⎕WC'Grid'(30 2⍴2/⍳30)
      F.G.RowTreeDepth←30⍴0 1 2 2
```


![gridtree1](../img/gridtree1.gif)


The user can interact with the tree images to expand and contract rows of the [Grid](./grid.md).


![gridtree2](../img/gridtree2.gif)



