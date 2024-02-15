




<h1 class="heading"><span class="name">ColLineTypes</span></h1>
| Applies To: | [Grid](./grid.md) |
| --- | ---  |

| Applies To: | [Grid](./grid.md) | [Grid](./grid.md) |  |  |
| --- | --- | ---  |
| [Grid](./grid.md) |  |  |


Description


This property specifies the appearance of the vertical grid lines in a [Grid](./grid.md) object.



ColLineTypes is an integer vector, whose length is normally equal to the number of columns in the [Grid](./grid.md). Each element in ColLineTypes specifies an index into the [GridLineFCol](gridlinefcol.md) and GridLineWidth properties, thus selecting the colour and width of the vertical grid lines.


For example, if ColLineTypes[1] is 3, the first vertical grid line in the [Grid](./grid.md) is displayed using the colour specified by the 3rd element of [GridLineFCol](gridlinefcol.md), and the width specified by the 3rd element of GridLineWidth.


Note that ColLineTypes is not `⎕IO` dependent, and the value 0 is treated the same as the value 1; both selecting the *first* colour and line width specified by [GridLineFCol](gridlinefcol.md) and GridLineWidth respectively.


The default value of ColLineTypes is an empty numeric vector (`⍬`). If so, all vertical grid lines are drawn using the first element of [GridLineFCol](gridlinefcol.md) and GridLineWidth.


A vertical grid line is drawn down the right edge of its associated column. One pixel is drawn *inside* the column of cells; additional pixels (if any) are drawn *between* that column of cells and the next one to its right.


