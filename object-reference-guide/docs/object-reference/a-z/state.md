




<h1 class="heading"><span class="name">State</span></h1>

| Applies To: | [Button](./button.md) | [Form](./form.md) | [SubForm](./subform.md) | [TabButton](./tabbutton.md) | [ToolButton](./toolbutton.md) |
| --- | --- | --- | --- | --- | ---  |


**Description**


This property determines the state of a [Button](./button.md), [TabButton](./tabbutton.md), [ToolButton](./toolbutton.md), [Form](./form.md), or [SubForm](./subform.md). It is a single number with the value 0 (the default), 1, or 2 ([Form](./form.md) and [SubForm](./subform.md)).


If the [Style](style.md) property is `'Push'`, a State of 0 means that the pushbutton is displayed normally (out). If its State is 1, the pushbutton is displayed depressed (in).


If the [Style](style.md) property is `'Radio'` or `'Check'`, 0 means "not selected" and 1 means "selected". Note that only one of a group of buttons with [Style ](style.md)`'Radio'` that share the same parent may have State 1. Setting State to 1 automatically deselects all the others in the group.


For a [Form](./form.md) or [SubForm](./subform.md), a value of State of 0 means that the [Form](./form.md) is currently displayed in its "normal" state. 1 means that the [Form](./form.md) is currently minimised (displayed as an icon). The value 2 indicates that the [Form](./form.md) is maximised and displayed full-screen. The State of a [Form](./form.md) can be changed using [`⎕WS`](../../Language/System Functions/ws.htm).



