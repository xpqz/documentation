




<h1 class="heading"><span class="name">ShowInput</span></h1>
| Applies To: | [Grid](../a-z/grid.md) |
| --- | ---  |

| Applies To: | [Grid](../a-z/grid.md) | [Grid](../a-z/grid.md) |  |  |
| --- | --- | ---  |
| [Grid](../a-z/grid.md) |  |  |


Description


This property specifies whether or not the cells in a [Grid](../a-z/grid.md) are displayed using their associated input objects.



The ShowInput property is either a single Boolean value that applies to all the cells in a [Grid](../a-z/grid.md), or it is a vector whose elements are mapped to individual cells via the [CellTypes](../a-z/celltypes.md) property. A value of 0 means that the corresponding cell is displayed normally. A value of 1 indicates that the cell is displayed using its associated input object, as it is when it is the current cell. ShowInput is relevant to cells displayed using [Combo](../a-z/combo.md) and [Button](../a-z/button.md) objects.



The example below illustrates the appearance of a [Grid](../a-z/grid.md) in which ShowInput is set to 0 for the Job Title column and 1 for the Region and Permanent columns.


![show1](../img/show1.gif)




The appearance of the same [Grid](../a-z/grid.md) but with ShowInput set to 0 throughout is illustrated below:


![show2](../img/show2.gif)



