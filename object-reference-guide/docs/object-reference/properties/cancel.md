




<h1 class="heading"><span class="name">Cancel</span></h1>

Applies To: [Button](../a-z/button.md)


**Description**


This property determines which (if any) Push button in a [Form](../a-z/form.md) or [SubForm](../a-z/subform.md) is to be associated with the Escape key. It has the value 1 or 0.


Pressing the Escape key will generate a [Select](../a-z/select.md) event on the [Button](../a-z/button.md) whose Cancel property is 1, regardless of which object has the keyboard focus.


As only one button in a [Form](../a-z/form.md) or [SubForm](../a-z/subform.md) can be the Cancel button, setting Cancel to 1 for a particular button automatically sets Cancel to 0 for all others in the same [Form](../a-z/form.md).



