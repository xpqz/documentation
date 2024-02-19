




<h1 class="heading"><span class="name">Select</span></h1>

**Applies To**



**Description**


For a [Button](../a-z/button.md) with [Style](../a-z/style.md)`'Push'` this event is generated when the user "pushes" the button. This can be done by clicking the left mouse button, or by pressing the Enter key or the space bar when the [Button](../a-z/button.md) has the focus. The Select event can also be generated when the [Button](../a-z/button.md) does not have the focus, by pressing the Enter key when its [Default](../a-z/default.md) property is 1 or by pressing the ESC key when its [Cancel](../a-z/cancel.md) property is 1.


For a [Button](../a-z/button.md) with [Style](../a-z/style.md)`'Radio'` or `'Check'` this event is generated when the user toggles the button from one state to another. This can be achieved by clicking the left mouse button or by pressing the space bar when the [Button](../a-z/button.md) has the focus.


For a [Combo](../a-z/combo.md) or [List](../a-z/list.md) object, a Select event is generated when the user selects an item from the list, whether by pressing the arrow keys or by clicking the left mouse button.


For a [MenuItem](../a-z/menuitem.md), a Select event is generated when the user chooses the item.


For all other objects, this event is generated when the user presses the keys associated with the object's [Accelerator](../a-z/accelerator.md) property.



The event message reported as the result of [`⎕DQ`](../../Language/System Functions/dq.htm), or supplied as the right argument to your callback function, is a 2-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | Event code |



