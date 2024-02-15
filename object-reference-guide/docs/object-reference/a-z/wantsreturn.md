




<h1 class="heading"><span class="name">WantsReturn</span></h1>
| Applies To: | [Edit](./edit.md) | [RichEdit](./richedit.md) |
| --- | --- | ---  |

| Applies To: | [Edit](./edit.md) [RichEdit](./richedit.md) | [Edit](./edit.md) | [RichEdit](./richedit.md) |  |
| --- | --- | ---  |
| [Edit](./edit.md) | [RichEdit](./richedit.md) |  |


Description


This Boolean property specifies the behaviour of the Enter key for a multi-line [Edit](./edit.md) (Style `'Multi'`) and a [RichEdit](./richedit.md) object.


A value of 0 means that the Enter key is ignored by the [Edit](./edit.md) or [RichEdit](./richedit.md). Instead, the Enter key will (if appropriate) cause a Select event on a Button in the same Form. The user must press Ctrl+Enter to input a new line.


A value of 1 means that pressing the Enter key will introduce a new line into the object.


WantsReturn must be established when the object is created by `⎕WC` and may not subsequently be altered using `⎕WS`. Its default value is 0 in an Edit and 1 in a RichEdit.



