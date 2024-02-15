



<h1 class="heading"><span class="name">RowSetVisibleDepth</span></h1>
| Applies To: | [Grid](../a-z/grid.md) |
| --- | ---  |

| Applies To: | [Grid](../a-z/grid.md) | [Grid](../a-z/grid.md) |  |  |
| --- | --- | ---  |
| [Grid](../a-z/grid.md) |  |  |


Description


This method is used to set the maximum visible depth of data in rows of a [Grid](../a-z/grid.md).


The argument to RowSetVisibleDepth is a numeric scalar as follows

| `[1]` | Depth | integer |
| --- | --- | ---  |


All rows in the grid that have a value of [RowTreeDepth](../a-z/rowtreedepth.md) less than or equal to *Depth* are expanded. Rows with a value of [RowTreeDepth](../a-z/rowtreedepth.md) greater than *Depth* are collapsed.


Note:[ Expanding](../a-z/expanding.md) and [Retracting](../a-z/retracting.md) events are not generated when this method is called.




#### Examples
```apl
      'F'⎕WC'Form' 'Grid: TreeView Feature'
      'F.G'⎕WC'Grid'(30 2⍴2/⍳30)
      F.G.RowTreeDepth←30⍴0 1 2 2
```


![gridtree1](../img/gridtree1.gif)
```apl
      F.G.RowSetVisibleDepth 1
```


![gridtree12](../img/gridtree12.gif)

```apl
      F.G.RowSetVisibleDepth 99
```


![gridtree13](../img/gridtree13.gif)


