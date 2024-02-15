




<h1 class="heading"><span class="name">ColChange</span></h1>
| Applies To: | [Grid](./grid.md) |
| --- | ---  |

| Applies To: | [Grid](./grid.md) | [Grid](./grid.md) |  |  |
| --- | --- | ---  |
| [Grid](./grid.md) |  |  |


Description


This method is used to change the data in a column of a [Grid](./grid.md).


The argument to ColChange is a 2-element array as follows:

| `[1]` | Column number | integer |
| --- | --- | ---  |
| `[2]` | Column data | array |


Note that the *Column data* must be a scalar or a vector whose length is equal to the number of rows in the [Grid](./grid.md). Its elements may be scalar numbers, character vectors or matrices.


