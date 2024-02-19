




<h1 class="heading"><span class="name">RowLineTypes</span></h1>

| Applies To: | [Grid](./grid.md) |
| --- | ---  |


**Description**


This property specifies the appearance of the horizontal grid lines in a [Grid](./grid.md) object.



RowLineTypes is an integer vector, whose length is normally equal to the number of rows in the [Grid](./grid.md). Each element in RowLineTypes specifies an index into the [GridLineFCol](gridlinefcol.md) and [GridLineWidth](GridLineWidth.htm) properties, thus selecting the colour and width of the horizontal grid lines.


For example, if RowLineTypes[1] is 3, the first horizontal grid line in the [Grid](./grid.md) is displayed using the colour specified by the 3rd element of [GridLineFCol](gridlinefcol.md), and the width specified by the 3rd element of [GridLineWidth](GridLineWidth.htm).


Note that RowLineTypes is not `⎕IO` dependent, and the value 0 is treated the same as the value 1; both selecting the *first* colour and line width specified by [GridLineFCol](gridlinefcol.md) and [GridLineWidth](GridLineWidth.htm) respectively.


The default value of RowLineTypes is an empty numeric vector (`⍬`). If so, all horizontal grid lines are drawn using the first element of [GridLineFCol](gridlinefcol.md) and [GridLineWidth](GridLineWidth.htm).


A horizontal grid line is drawn along the bottom edge of its associated row. One pixel is drawn *inside* the row of cells; additional pixels (if any) are drawn *between* that row of cells and the next one below.


