




<h1 class="heading"><span class="name">MDIActivate</span></h1>

| Applies To: | [SubForm](../a-z/subform.md) |
| --- | ---  |


**Description**


This event is generated when the user activates a particular [SubForm](../a-z/subform.md) that is the child of an [MDIClient](../a-z/mdiclient.md). This occurs when the user clicks the left mouse button in the [SubForm](../a-z/subform.md) or selects it from the menu nominated for this purpose (see [MDIMenu](../a-z/mdimenu.md) property). You may also call MDIActivate as a method.


Note that this event is reported after the action has taken place and cannot be disabled by returning 0 from a callback function or by setting its action code to `¯1`.


The event message reported as the result of [`⎕DQ`](../../Language/System Functions/dq.htm), or supplied as the right argument to your callback function, is a 3-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'MDIActivate'` or 42 |
| `[3]` | Object name | character vector |


Note that the 3rd element of the event message is either an empty vector or contains the name of the [SubForm](../a-z/subform.md) that was previously the active one in the same [MDIClient](../a-z/mdiclient.md).



