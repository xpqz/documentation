



<h1 class="heading"><span class="name">RowSetVisibleDepth</span></h1>
| Applies To: | [Grid](./grid.md) |
| --- | ---  |

| Applies To: | [Grid](./grid.md) | [Grid](./grid.md) |  |  |
| --- | --- | ---  |
| [Grid](./grid.md) |  |  |


Description


This method is used to set the maximum visible depth of data in rows of a [Grid](./grid.md).


The argument to RowSetVisibleDepth is a numeric scalar as follows

| `[1]` | Depth | integer |
| --- | --- | ---  |


All rows in the grid that have a value of [RowTreeDepth](./rowtreedepth.md) less than or equal to *Depth* are expanded. Rows with a value of [RowTreeDepth](./rowtreedepth.md) greater than *Depth* are collapsed.


Note:[ Expanding](./expanding.md) and [Retracting](./retracting.md) events are not generated when this method is called.




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


