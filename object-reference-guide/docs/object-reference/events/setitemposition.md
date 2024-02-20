




<h1 class="heading"><span class="name">SetItemPosition</span></h1>

Applies To: [ListView](../a-z/listview.md)


**Description**


If enabled, this event is reported when the user drag-drops an item within a [ListView](../a-z/listview.md) object. This operation may be disabled by returning 0 from a callback function.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 7-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'SetItemPosition'` or 322 |
| `[3]` | Item number | Integer. The index of the item. |
| `[4]` | Y-position | Integer. New y-position of the item. |
| `[5]` | X-position | Integer. New x-position of the item. |
| `[6]` | Button number | Integer. The mouse button used to perform the drag. |
| `[7]` | Shift State | Integer: Sum of shift key codes (number) 1 =        Shift key is down 2 = Ctrl key is down 4 =    Alt key is down |



