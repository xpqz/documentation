




<h1 class="heading"><span class="name">DropDown</span></h1>

**Applies To**


**Description**


If enabled, this event is reported when the user clicks the drop-down button in a  [Combo](./combo.md), [ComboEx](./comboex.md), [ColorButton](./colorbutton.md), [DateTimePicker](./datetimepicker.md) or [Menu](./menu.md) object, just before the drop-down list, colour selection, calendar or -menu is displayed.



For a [Button](./button.md) this event only applies if the Style of the [Button](./button.md) is `Split`. For such a [Button](./button.md) and for the [ButtonEdit](./buttonedit.md) object there is no default processing for the event and it is the responsibility of the programmer to take appropriate action in a call-back function.


For a [DateTimePicker](./datetimepicker.md) this event only applies if the Style of the [DateTimePicker](./datetimepicker.md) is `'Combo'`.



The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'DropDown'` or 45 |



This event is reported for information only and cannot be disabled or modified in any way.


The associated callback is run **immediately** while the windows notification is still on the stack. See 
Interface Guide: 

High-Priority Callback FunctionsHigh-Priority Callback Functions on page 1.


