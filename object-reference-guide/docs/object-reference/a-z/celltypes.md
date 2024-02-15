




<h1 class="heading"><span class="name">CellTypes</span></h1>
| Applies To: | [Grid](./grid.md) |
| --- | ---  |

| Applies To: | [Grid](./grid.md) | [Grid](./grid.md) |  |  |
| --- | --- | ---  |
| [Grid](./grid.md) |  |  |


Description


This property specifies the type of each cell in a [Grid](./grid.md) object. It is a matrix whose elements are origin-1 indices into other property arrays ([FCol](fcol.md), [BCol](bcol.md), [CellFonts](cellfonts.md) and [Input](input.md)).


For example, if CellTypes[1;1] is 3, the first cell in the [Grid](./grid.md) is displayed using the foreground colour specified by the 3rd element of [FCol](fcol.md), the background colour specified by the 3rd element of [BCol](bcol.md), and so forth. Note however that scalar property arrays are extended if necessary. Therefore if you require 5 different foreground colours but only one background colour, [BCol](bcol.md) need specify only a single colour.


You can dynamically change a single element of CellTypes using the [SetCellType](./setcelltype.md) method.



