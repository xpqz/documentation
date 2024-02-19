




<h1 class="heading"><span class="name">Default</span></h1>

| Applies To: | [Button](./button.md) | [MsgBox](./msgbox.md) |
| --- | --- | ---  |


**Description**


This property determines which of a set of push buttons in a [Form](./form.md), [SubForm](./subform.md) or [MsgBox](./msgbox.md) is the default button.



In a [Form](./form.md) or [SubForm](./subform.md), the Default [Button](./button.md) will generate a [Select](./select.md) event (30) when the user presses the Enter key, even though the Default [Button](./button.md) may not have the focus at the time.


If however, the user explicitly shifts the focus to another Push [Button](./button.md), the automatic selection of the Default [Button](./button.md) is disabled and the Enter key applies to the [Button](./button.md) with the focus.


For a [Button](./button.md), the Default property has the value 1 or 0. As only one [Button](./button.md) can be the Default [Button](./button.md), setting Default to 1 for a particular [Button](./button.md) automatically sets Default to 0 for all others with the same parent.


In a [MsgBox](./msgbox.md), Default specifies which button initially has the focus. It has the value 1, 2 or 3 corresponding to the three buttons that can be defined. See [Btns](Btns.htm) property for further details.


