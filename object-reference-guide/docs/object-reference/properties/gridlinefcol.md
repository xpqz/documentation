




<h1 class="heading"><span class="name">GridLineFCol</span></h1>

| Applies To: | [Grid](../a-z/grid.md) |
| --- | ---  |


**Description**


The GridLineFCol property specifies the colours of the grid lines in a [Grid](../a-z/grid.md) object. GridLineFCol should be used if different coloured grid lines are required. If all the grid lines are the same colour, use [GridFCol](../a-z/gridfcol.md).



GridLineFCol may be a scalar or a vector. Each item may be a 3-element vector of integer values in the range 0-255 which refer to the red, green and blue components of the colour respectively, or a scalar that defines a standard Windows colour element (see [BCol](../a-z/bcol.md) for details). Note that a single RGB triplet must be enclosed.


The default value of GridLineFCol is an empty numeric vector (`⍬`). If so, all the grid lines are drawn using the single colour specified by [GridFCol](../a-z/gridfcol.md).


Unlike [GridFCol](../a-z/gridbcol.md), setting GridLineFCol overrides the colour which would be used if **Native Look and Feel** was enabled.


Elements of GridLineFCol are allocated to individual grid lines via the [RowLineTypes](../a-z/rowlinetypes.md) and [ColLineTypes](../a-z/collinetypes.md) properties.


See also: [GridLineWidth](../a-z/gridlinewidth.md).


