




<h1 class="heading"><span class="name">GridLineFCol</span></h1>
| Applies To: | [Grid](./grid.md) |
| --- | ---  |

| Applies To: | [Grid](./grid.md) | [Grid](./grid.md) |  |  |
| --- | --- | ---  |
| [Grid](./grid.md) |  |  |


Description


The GridLineFCol property specifies the colours of the grid lines in a [Grid](./grid.md) object. GridLineFCol should be used if different coloured grid lines are required. If all the grid lines are the same colour, use GridFCol.



GridLineFCol may be a scalar or a vector. Each item may be a 3-element vector of integer values in the range 0-255 which refer to the red, green and blue components of the colour respectively, or a scalar that defines a standard Windows colour element (see BCol for details). Note that a single RGB triplet must be enclosed.


The default value of GridLineFCol is an empty numeric vector (`⍬`). If so, all the grid lines are drawn using the single colour specified by GridFCol.


Unlike GridFCol, setting GridLineFCol overrides the colour which would be used if **Native Look and Feel** was enabled.


Elements of GridLineFCol are allocated to individual grid lines via the RowLineTypes and ColLineTypes properties.


See also: GridLineWidth.


