




<h1 class="heading"><span class="name">MouseUp</span></h1>

**Applies To**


**Description**


If enabled, this event is reported when the user releases one of the mouse buttons. The event message reported as the result of [`⎕DQ`](../../Language/System%20Functions/dq.htm), or supplied as the right argument to your callback function, is a 6-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'MouseUp'` or 2 |
| `[3]` | Y | y-position of mouse (number) |
| `[4]` | X | x-position of mouse (number) |
| `[5]` | Button | button released (number) 1 = left button 2 = right button 4 = middle button |
| `[6]` | Shift State | sum of shift key codes (number) 1 = Shift key is down 2 = Ctrl key is down |


In a graphical object ([Circle](../a-z/circle.md), [Ellipse](../a-z/ellipse.md), [Image](../a-z/image.md), [Marker](../a-z/marker.md), [Poly](../a-z/poly.md) and [Rect](../a-z/rect.md)), the position of the mouse is reported relative to the top-left corner of its bounding rectangle.



