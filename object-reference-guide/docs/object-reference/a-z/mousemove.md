




<h1 class="heading"><span class="name">MouseMove</span></h1>

**Applies To**


**Description**


If enabled, this event is reported when the user moves the mouse. The event message reported as the result of [`⎕DQ`](../../Language/System%20Functions/dq.htm), or supplied as the right argument to your callback function, is a 6-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'MouseMove'` or 3 |
| `[3]` | Y | y-position of mouse (number) |
| `[4]` | X | x-position of mouse (number) |
| `[5]` | Button | button released (number) 1 = left button 2 = right button 4 = middle button |
| `[6]` | Shift State | sum of shift key codes (number) 1 = Shift key is down 2 = Ctrl key is down |


In a graphical object ([Circle](./circle.md), [Ellipse](./ellipse.md), [Image](./image.md), [Marker](./marker.md), [Poly](./poly.md) and [Rect](./rect.md)), the position of the mouse is reported relative to the top-left corner of its bounding rectangle.


Note that rapid movement of the mouse will not necessarily cause an overwhelming number of MouseMove events to be reported, as several small movements are automatically combined into one large one.



