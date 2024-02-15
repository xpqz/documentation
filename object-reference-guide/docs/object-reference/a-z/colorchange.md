




<h1 class="heading"><span class="name">ColorChange</span></h1>
| Applies To: | [ColorButton](./colorbutton.md) |
| --- | ---  |

| Applies To: | [ColorButton](./colorbutton.md) | [ColorButton](./colorbutton.md) |  |  |
| --- | --- | ---  |
| [ColorButton](./colorbutton.md) |  |  |


Description


If enabled, this event is reported by a [ColorButton](./colorbutton.md) object when the user chooses a colour from the colour selection drop-down.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 3-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | 'ColorChange' or 430 |
| `[3]` | New Colour | 3-element integer vector |


The 3rd element of the event message contains the RGB value for the selected colour.


Note that the event is reported when the user chooses a colour, whether or not the newly selected colour differs from the one that was previously selected.


This event is reported for information only and cannot be disabled or modified in any way.



