




<h1 class="heading"><span class="name">RowLineTypes</span></h1>
| Applies To: | [Grid](../a-z/grid.md) |
| --- | ---  |

| Applies To: | [Grid](../a-z/grid.md) | [Grid](../a-z/grid.md) |  |  |
| --- | --- | ---  |
| [Grid](../a-z/grid.md) |  |  |


Description


This property specifies the appearance of the horizontal grid lines in a [Grid](../a-z/grid.md) object.



RowLineTypes is an integer vector, whose length is normally equal to the number of rows in the [Grid](../a-z/grid.md). Each element in RowLineTypes specifies an index into the [GridLineFCol](../a-z/gridlinefcol.md) and [GridLineWidth](../a-z/gridlinewidth.md) properties, thus selecting the colour and width of the horizontal grid lines.


For example, if RowLineTypes[1] is 3, the first horizontal grid line in the [Grid](../a-z/grid.md) is displayed using the colour specified by the 3rd element of [GridLineFCol](../a-z/gridlinefcol.md), and the width specified by the 3rd element of [GridLineWidth](../a-z/gridlinewidth.md).


Note that RowLineTypes is not `⎕IO` dependent, and the value 0 is treated the same as the value 1; both selecting the *first* colour and line width specified by [GridLineFCol](../a-z/gridlinefcol.md) and [GridLineWidth](../a-z/gridlinewidth.md) respectively.


The default value of RowLineTypes is an empty numeric vector (`⍬`). If so, all horizontal grid lines are drawn using the first element of [GridLineFCol](../a-z/gridlinefcol.md) and [GridLineWidth](../a-z/gridlinewidth.md).


A horizontal grid line is drawn along the bottom edge of its associated row. One pixel is drawn *inside* the row of cells; additional pixels (if any) are drawn *between* that row of cells and the next one below.


