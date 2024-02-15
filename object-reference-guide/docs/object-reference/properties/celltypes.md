




<h1 class="heading"><span class="name">CellTypes</span></h1>

| Applies To: | [Grid](../a-z/grid.md) |
| --- | ---  |


**Description**


This property specifies the type of each cell in a [Grid](../a-z/grid.md) object. It is a matrix whose elements are origin-1 indices into other property arrays ([FCol](../a-z/fcol.md), [BCol](../a-z/bcol.md), [CellFonts](../a-z/cellfonts.md) and [Input](../a-z/input.md)).


For example, if CellTypes[1;1] is 3, the first cell in the [Grid](../a-z/grid.md) is displayed using the foreground colour specified by the 3rd element of [FCol](../a-z/fcol.md), the background colour specified by the 3rd element of [BCol](../a-z/bcol.md), and so forth. Note however that scalar property arrays are extended if necessary. Therefore if you require 5 different foreground colours but only one background colour, [BCol](../a-z/bcol.md) need specify only a single colour.


You can dynamically change a single element of CellTypes using the [SetCellType](../a-z/setcelltype.md) method.



