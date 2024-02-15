



<h1 class="heading"><span class="name">GestureTwoFingerTap</span></h1>

Applies To

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) [Animation](../a-z/animation.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [ColorButton](../a-z/colorbutton.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Form](../a-z/form.md) [Group](../a-z/group.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [MDIClient](../a-z/mdiclient.md) [ProgressBar](../a-z/progressbar.md) [PropertyPage](../a-z/propertypage.md) [RichEdit](../a-z/richedit.md) [Scroll](../a-z/scroll.md) [Spinner](../a-z/spinner.md) [SubForm](../a-z/subform.md) [TreeView](../a-z/treeview.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Group](../a-z/group.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) | [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [Spinner](../a-z/spinner.md) | [SubForm](../a-z/subform.md) | [TreeView](../a-z/treeview.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) |
| [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) |
| [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) |
| [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Group](../a-z/group.md) |
| [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) |
| [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [RichEdit](../a-z/richedit.md) |
| [Scroll](../a-z/scroll.md) | [Spinner](../a-z/spinner.md) | [SubForm](../a-z/subform.md) |
| [TreeView](../a-z/treeview.md) |  |  |


Description


This event is reported when the user taps two fingers at the same time on an object


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 5-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'GestureTwoFingerTap'` or 496 |
| `[3]` | Flags | integer which reports the state of the gesture |
| `[4]` | Location | 2-element integer vector containing the y and x-position respectively of the point midway between the two fingers. These are reported in pixel coordinates relative to the origin (top-left corner) of the object reporting the event.. |
| `[5]` | Distance | 2-element integer vector containing the high and low parts (words) of a 64-bit integer that indicates the distance between the two fingers. |


The Flags parameter [3] which reports the state of the Gesture, is always an integer with the value 5 (**GF_BEGIN+GF_END**).

| Name | Value | Description |
| --- | --- | ---  |
| GF_BEGIN | 1 | A gesture is starting. |
| GF_END | 4 | A gesture has finished. |


Returning zero from the callback disables any default handling by the operating system.


The associated callback is run immediately while the windows notification is still on the stack. See 
Interface Guide: 

High-Priority Callback FunctionsHigh-Priority Callback Functions on page 1.


