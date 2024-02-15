




<h1 class="heading"><span class="name">Text</span></h1>

Applies To

| Applies To: | [Detach](../a-z/detach.md) [ChooseFont](../a-z/choosefont.md) | [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| --- | --- | ---  |
| [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |


Description


This property is associated with the text contents of an object and is a character array.



In a [ButtonEdit](../a-z/buttonedit.md), [Combo](../a-z/combo.md), [StatusField](../a-z/statusfield.md), [Spinner](../a-z/spinner.md), or a single-line [Edit](../a-z/edit.md) object, Text may be a simple scalar or a simple vector.


In a [RichEdit](../a-z/richedit.md), a multi-line [Edit](../a-z/edit.md) field or in a [MsgBox](../a-z/msgbox.md), the value of Text may also be a simple matrix, or a vector of vectors. If so, "new-line" characters are appended to each row of the matrix, or to each vector in a vector of vectors, before being displayed. The user may insert or add a "new-line" character in a multi-line [Edit](../a-z/edit.md) by pressing Ctrl-Enter (Enter itself is used to press [Button](../a-z/button.md)s).


Note that if word-wrapping is in effect in a multi-line [Edit](../a-z/edit.md) object, the structure of Text does not correspond to the lines displayed.


In a [Text](../a-z/text.md) object, the value of the Text property may be a simple scalar, an enclosed vector or matrix, a simple vector, a simple matrix, or a vector of enclosed vectors or matrices.


In general, the value of Text returned by `⎕WG` has the same structure that was assigned to it by `⎕WC` or by the most recent call to `⎕WS`. New-Line characters entered by the users are removed.


You can copy text into the Windows [Clipboard](../a-z/clipboard.md) by using `⎕WS` to set Text for a [Clipboard](../a-z/clipboard.md) object. In this case you may specify a simple character scalar, vector or matrix, or a vector of character vectors. If you are retrieving data from the clipboard that has been stored by another application, Text will be either a character vector or a vector of character vectors.


The Text property of a [StatusField](../a-z/statusfield.md) is updated automatically if its [Style](../a-z/style.md) property is set to monitor the status of a key.


