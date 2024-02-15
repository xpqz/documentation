




<h1 class="heading"><span class="name">Default</span></h1>

| Applies To: | [Button](../a-z/button.md) | [MsgBox](../a-z/msgbox.md) |
| --- | --- | ---  |


**Description**


This property determines which of a set of push buttons in a [Form](../a-z/form.md), [SubForm](../a-z/subform.md) or [MsgBox](../a-z/msgbox.md) is the default button.



In a [Form](../a-z/form.md) or [SubForm](../a-z/subform.md), the Default [Button](../a-z/button.md) will generate a [Select](../a-z/select.md) event (30) when the user presses the Enter key, even though the Default [Button](../a-z/button.md) may not have the focus at the time.


If however, the user explicitly shifts the focus to another Push [Button](../a-z/button.md), the automatic selection of the Default [Button](../a-z/button.md) is disabled and the Enter key applies to the [Button](../a-z/button.md) with the focus.


For a [Button](../a-z/button.md), the Default property has the value 1 or 0. As only one [Button](../a-z/button.md) can be the Default [Button](../a-z/button.md), setting Default to 1 for a particular [Button](../a-z/button.md) automatically sets Default to 0 for all others with the same parent.


In a [MsgBox](../a-z/msgbox.md), Default specifies which button initially has the focus. It has the value 1, 2 or 3 corresponding to the three buttons that can be defined. See [Btns](../a-z/btns.md) property for further details.


