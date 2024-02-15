




<h1 class="heading"><span class="name">GridCopyError</span></h1>
| Applies To: | [Grid](../a-z/grid.md) |
| --- | ---  |

| Applies To: | [Grid](../a-z/grid.md) | [Grid](../a-z/grid.md) |  |  |
| --- | --- | ---  |
| [Grid](../a-z/grid.md) |  |  |


Description


If enabled, this event is reported when the user presses Ctrl+Insert and there is more than one block of selected cells in the [Grid](../a-z/grid.md) and the blocks are non-conformable. The default action of the event is to generate a Beep. Setting the action code of this event to `¯1`, or returning a 0 from a callback function attached to it, disables the Beep.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 5-element vector as follows:

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'GridCopyError'` or 196 |
| `[3]` |  | Zilde |
| `[4]` |  | Zilde |
| `[5]` | Start | A 2-column integer matrix whose rows identify the address of the first cell (row, column) of each of the selected blocks of cells. |
| `[6]` | End | A 2-column integer matrix whose rows identify the address of the last cell (row, column) of each of the selected blocks of cells. |


Note that the values of Start and End are sensitive to the index origin, `⎕IO`.



