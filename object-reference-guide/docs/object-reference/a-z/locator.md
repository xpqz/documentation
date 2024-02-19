




<h1 class="heading"><span class="name">Locator</span></h1>

| Applies To: | [Locator](./locator.md) |
| --- | ---  |


**Description**


If enabled, this event is generated when the user releases a mouse button, or presses any key (other than a cursor movement key) during a [`⎕DQ`](../../Language/System Functions/dq.htm) on a [Locator](./locator.md) object.


The event message reported as the result of [`⎕DQ`](../../Language/System Functions/dq.htm), or supplied as the right argument to your callback function, is a 9-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'Locator'` or 80 |
| `[3]` | Y | y-position of [Locator](./locator.md) after [`⎕DQ`](../../Language/System Functions/dq.htm) |
| `[4]` | X | x-position of [Locator](./locator.md) after [`⎕DQ`](../../Language/System Functions/dq.htm) |
| `[5]` | H | height of [Locator](./locator.md) after [`⎕DQ`](../../Language/System Functions/dq.htm) |
| `[6]` | W | width of [Locator](./locator.md) after [`⎕DQ`](../../Language/System Functions/dq.htm) |
| `[7]` | Mouse Button | number of the button which was released (0 if keystroke) |
| `[8]` | Keystroke | character scalar or vector containing the "Input Code" for the key that terminated the operation |
| `[9]` | Shift state | integer scalar |



