




<h1 class="heading"><span class="name">GridLineWidth</span></h1>

Applies To: [Grid](../a-z/grid.md)


**Description**


The GridLineWidth property specifies the widths in pixels of the grid lines in a [Grid](../a-z/grid.md) object.



GridLineWidth may be an integer scalar or a vector. Its default value is an empty numeric vector (`⍬`). If so, grid lines are drawn 1-pixel wide.


Grid lines are always displayed so that 1 pixel is drawn *within* the cell. If the width is greater than 1 pixel, the additional pixels are drawn *between* the cells.


If an element of GridLineWidth is 0, the corresponding grid lines are not drawn.


Elements of GridLineWidth are allocated to individual grid lines via the [RowLineTypes](../a-z/rowlinetypes.md) and [ColLineTypes](../a-z/collinetypes.md) properties.


See also: [GridLineFCol](../a-z/gridlinefcol.md).


