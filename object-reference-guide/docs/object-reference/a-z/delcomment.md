




<h1 class="heading"><span class="name">DelComment</span></h1>
| Applies To: | [Grid](./grid.md) |
| --- | ---  |

| Applies To: | [Grid](./grid.md) | [Grid](./grid.md) |  |  |
| --- | --- | ---  |
| [Grid](./grid.md) |  |  |


Description


This method is used to delete a comment from a [Grid](./grid.md).


The argument to DelComment is a 2 array as follows or `⍬`:

| `[1]` | Row | integer |
| --- | --- | ---  |
| `[2]` | Column | integer |


For example, the following expression removes the comment associated with the cell at row 2, column 1.
```apl
      F.C.DelComment 2 1
```


Note that to delete a comment associated with a row or column *title*, the appropriate element in the argument should be `¯1`.


If the argument is `⍬`, all comments are deleted.



