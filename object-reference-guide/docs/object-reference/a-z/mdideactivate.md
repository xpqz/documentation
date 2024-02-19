




<h1 class="heading"><span class="name">MDIDeactivate</span></h1>

| Applies To: | [SubForm](./subform.md) |
| --- | ---  |


**Description**


This event is generated when the user activates a different [SubForm](./subform.md) that is the child of an [MDIClient](./mdiclient.md), thereby de-activating the current one which causes this event. This occurs when the user clicks the left mouse button in another [SubForm](./subform.md) or selects it from the menu nominated for this purpose (see [MDIMenu](./mdimenu.md) property). You may also call MDIDeactivate as a method.


Note that this event is reported after the action has taken place and cannot be disabled by returning 0 from a callback function or by setting its action code to `¯1`.


The event message reported as the result of [`⎕DQ`](../../Language/System Functions/dq.htm), or supplied as the right argument to your callback function, is a 3-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'MDIDeactivate'` or 43 |
| `[3]` | Object name | character vector |


Note that the 3rd element of the event message contains the name of the [SubForm](./subform.md) that has now been made the active one in the same [MDIClient](./mdiclient.md).



