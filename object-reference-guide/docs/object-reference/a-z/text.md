




<h1 class="heading"><span class="name">Text</span></h1>

**Applies To**


**Description**


This property is associated with the text contents of an object and is a character array.



In a [ButtonEdit](./buttonedit.md), [Combo](./combo.md), [StatusField](./statusfield.md), [Spinner](./spinner.md), or a single-line [Edit](./edit.md) object, Text may be a simple scalar or a simple vector.


In a [RichEdit](./richedit.md), a multi-line [Edit](./edit.md) field or in a [MsgBox](./msgbox.md), the value of Text may also be a simple matrix, or a vector of vectors. If so, "new-line" characters are appended to each row of the matrix, or to each vector in a vector of vectors, before being displayed. The user may insert or add a "new-line" character in a multi-line [Edit](./edit.md) by pressing Ctrl-Enter (Enter itself is used to press [Button](./button.md)s).


Note that if word-wrapping is in effect in a multi-line [Edit](./edit.md) object, the structure of Text does not correspond to the lines displayed.


In a [Text](./text.md) object, the value of the Text property may be a simple scalar, an enclosed vector or matrix, a simple vector, a simple matrix, or a vector of enclosed vectors or matrices.


In general, the value of Text returned by [`⎕WG`](../../Language/System Functions/wg.htm) has the same structure that was assigned to it by [`⎕WC`](../../Language/System Functions/wc.htm) or by the most recent call to [`⎕WS`](../../Language/System Functions/ws.htm). New-Line characters entered by the users are removed.


You can copy text into the Windows [Clipboard](./clipboard.md) by using [`⎕WS`](../../Language/System Functions/ws.htm) to set Text for a [Clipboard](./clipboard.md) object. In this case you may specify a simple character scalar, vector or matrix, or a vector of character vectors. If you are retrieving data from the clipboard that has been stored by another application, Text will be either a character vector or a vector of character vectors.


The Text property of a [StatusField](./statusfield.md) is updated automatically if its [Style](style.md) property is set to monitor the status of a key.


