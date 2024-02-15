




<h1 class="heading"><span class="name">ShowBalloonTip</span></h1>
| Applies To: | [SysTrayItem](./systrayitem.md) |
| --- | ---  |

| Applies To: | [SysTrayItem](./systrayitem.md) | [SysTrayItem](./systrayitem.md) |  |  |
| --- | --- | ---  |
| [SysTrayItem](./systrayitem.md) |  |  |


Description


The ShowBalloonTip method displays a BalloonTip in a [SysTrayItem](./systrayitem.md) object.


The argument to ShowBalloonTip is a  1, 2, 3 or 4-element array as follows:

| `[1]` | Title | character vector |
| --- | --- | ---  |
| `[2]` | Text | character vector or matrix |
| `[3]` | Icon | Integer scalar,  a character vector or a ref |
| `[4]` | Flags | Integer |


The **Title** parameter is the text to be displayed in the BalloonTip title (maximum length 64).


The **Text** parameter is the text (maximum length 256) to be displayed in the BalloonTip. If omitted or empty, the BalloonTip is not displayed.


If the **Icon** parameter is an integer, it means:

| 0 | No icon |
| --- | ---  |
| 1 | Information icon |
| 2 | Warning icon |
| 3 | Error icon |


Other values represent the name or a ref to an [Icon](./icon.md) object. If the **Icon** parameter is omitted, no icon is displayed in the BalloonTip.


If the **Icon** parameter specifies a *large* Icon object (32 x 32 bits) the Flags parameter must be 32. Otherwise this parameter is not used.



