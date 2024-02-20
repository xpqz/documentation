




<h1 class="heading"><span class="name">MaxLength</span></h1>

Applies To: [ButtonEdit](./buttonedit.md) [Edit](./edit.md) [Spinner](./spinner.md)


**Description**


This property specifies the maximum number of characters that the user may enter in a single-line [Edit](./edit.md) object ( [Style](style.md) `'Single'`) or in the edit field associated with a [Spinner](./spinner.md). It does not apply to a multi-line [Edit](./edit.md) object ([Style ](style.md)`'Multi'`). MaxLength does not limit the length of the vector that you may assign to the [Text](text.md) property using [`⎕WC`](../../Language/System Functions/wc.htm) or [`⎕WS`](../../Language/System Functions/ws.htm). However, if you overfill the field in this way, the user must delete excess characters before the object will accept further input.



