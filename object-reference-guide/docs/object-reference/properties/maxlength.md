




<h1 class="heading"><span class="name">MaxLength</span></h1>
| Applies To: | [ButtonEdit](../a-z/buttonedit.md) | [Edit](../a-z/edit.md) | [Spinner](../a-z/spinner.md) |
| --- | --- | --- | ---  |

| Applies To: | [ButtonEdit](../a-z/buttonedit.md) [Edit](../a-z/edit.md) [Spinner](../a-z/spinner.md) | [ButtonEdit](../a-z/buttonedit.md) | [Edit](../a-z/edit.md) | [Spinner](../a-z/spinner.md) |
| --- | --- | ---  |
| [ButtonEdit](../a-z/buttonedit.md) | [Edit](../a-z/edit.md) | [Spinner](../a-z/spinner.md) |


Description


This property specifies the maximum number of characters that the user may enter in a single-line [Edit](../a-z/edit.md) object ( [Style](../a-z/style.md) `'Single'`) or in the edit field associated with a [Spinner](../a-z/spinner.md). It does not apply to a multi-line [Edit](../a-z/edit.md) object ([Style ](../a-z/style.md)`'Multi'`). MaxLength does not limit the length of the vector that you may assign to the [Text](../a-z/text.md) property using `⎕WC` or `⎕WS`. However, if you overfill the field in this way, the user must delete excess characters before the object will accept further input.



