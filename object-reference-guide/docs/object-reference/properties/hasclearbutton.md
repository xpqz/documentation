




<h1 class="heading"><span class="name">HasClearButton</span></h1>
| Applies To: | [ButtonEdit](../a-z/buttonedit.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [Edit](../a-z/edit.md) |
| --- | --- | --- | --- | ---  |

| Applies To: | [ButtonEdit](../a-z/buttonedit.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [Edit](../a-z/edit.md) | [ButtonEdit](../a-z/buttonedit.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [Edit](../a-z/edit.md) |  |  |
| --- | --- | ---  |
| [ButtonEdit](../a-z/buttonedit.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) |
| [Edit](../a-z/edit.md) |  |  |


Description


Specifies whether or not an![clearbutton](../img/clearbutton.png)button is displayed in the right-hand end of an edit box. Clicking this button clears the text from the field.



HasClearButton is Boolean. 1 means that an ![clearbutton](../img/clearbutton.png) button will be displayed; 0 (the default) means that the button will not be shown. It may only be specified when the object is created. If you subsequently attempt to change the value of HasClearButton, the operation will fail with `NONCE ERROR`.


HasClearButton is only effective for Edit objects with Style Single; it is silently ignored for other Styles of Edit objects.


![hasclearbutton](../img/hasclearbutton.png)


Note that this feature only applies if Native Look and Feel 
(see page 1)
 is enabled.


