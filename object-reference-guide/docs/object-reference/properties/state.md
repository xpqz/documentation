




<h1 class="heading"><span class="name">State</span></h1>

| Applies To: | [Button](../a-z/button.md) | [Form](../a-z/form.md) | [SubForm](../a-z/subform.md) | [TabButton](../a-z/tabbutton.md) | [ToolButton](../a-z/toolbutton.md) |
| --- | --- | --- | --- | --- | ---  |


**Description**


This property determines the state of a [Button](../a-z/button.md), [TabButton](../a-z/tabbutton.md), [ToolButton](../a-z/toolbutton.md), [Form](../a-z/form.md), or [SubForm](../a-z/subform.md). It is a single number with the value 0 (the default), 1, or 2 ([Form](../a-z/form.md) and [SubForm](../a-z/subform.md)).


If the [Style](../a-z/style.md) property is `'Push'`, a State of 0 means that the pushbutton is displayed normally (out). If its State is 1, the pushbutton is displayed depressed (in).


If the [Style](../a-z/style.md) property is `'Radio'` or `'Check'`, 0 means "not selected" and 1 means "selected". Note that only one of a group of buttons with [Style ](../a-z/style.md)`'Radio'` that share the same parent may have State 1. Setting State to 1 automatically deselects all the others in the group.


For a [Form](../a-z/form.md) or [SubForm](../a-z/subform.md), a value of State of 0 means that the [Form](../a-z/form.md) is currently displayed in its "normal" state. 1 means that the [Form](../a-z/form.md) is currently minimised (displayed as an icon). The value 2 indicates that the [Form](../a-z/form.md) is maximised and displayed full-screen. The State of a [Form](../a-z/form.md) can be changed using [`⎕WS`](../../Language/System Functions/ws.htm).



