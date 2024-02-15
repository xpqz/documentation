



<h1 class="heading"><span class="name">GestureZoom</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Animation](./animation.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Form](./form.md) [Group](./group.md) [List](./list.md) [ListView](./listview.md) [MDIClient](./mdiclient.md) [ProgressBar](./progressbar.md) [PropertyPage](./propertypage.md) [RichEdit](./richedit.md) [Scroll](./scroll.md) [Spinner](./spinner.md) [SubForm](./subform.md) [TreeView](./treeview.md) | [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) | [Group](./group.md) | [List](./list.md) | [ListView](./listview.md) | [MDIClient](./mdiclient.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [Spinner](./spinner.md) | [SubForm](./subform.md) | [TreeView](./treeview.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) |
| [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) |
| [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) |
| [Edit](./edit.md) | [Form](./form.md) | [Group](./group.md) |
| [List](./list.md) | [ListView](./listview.md) | [MDIClient](./mdiclient.md) |
| [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [RichEdit](./richedit.md) |
| [Scroll](./scroll.md) | [Spinner](./spinner.md) | [SubForm](./subform.md) |
| [TreeView](./treeview.md) |  |  |


Description


This event is reported when the user touches  two fingers on an object and moves them apart or towards each other.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 5-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'GestureZoom'` or 493 |
| `[3]` | Flags | integer which reports the state of the gesture |
| `[4]` | Location | 2-element integer vector containing the y and x-position respectively of the centre point of the zoom (the point midway between the two fingers). These are reported in pixel coordinates relative to the origin (top-left corner) of the object reporting the event. |
| `[5]` | Distance | 2-element integer vector containing the high and low parts (words) of a 64-bit integer that indicates the distance between the two fingers. |


The Flags parameter [3] which reports the state of the Gesture, is an integer with the value 0, 1 (**GF_BEGIN**),or 4 (**GF_END**) with the following meanings:

| Name | Value | Description |
| --- | --- | ---  |
|  | 0 | A gesture is in progress |
| GF_BEGIN | 1 | A gesture is starting. |
| GF_END | 4 | A gesture has finished. |


When the user first touches two fingers on an object and begins to move them apart or towards each other, the object generates a GestureZoom event with a `Flags` parameter of 1 (GF_BEGIN). As the user continues to moves the fingers apart or towards each other, the object generates a series of GestureZoom events with a `Flags` parameter of 0.  When the user lifts one or both fingers away, the object generates it generates a final GestureZoom event, with a `Flags` parameter of 4 (GF_END).


No other event will be reported between the start and end of a series of GestureZoom events.


Returning zero from the callback disables any default handling by the operating system.


The associated callback is run immediately while the windows notification is still on the stack. See 
Interface Guide: 

High-Priority Callback FunctionsHigh-Priority Callback Functions on page 1.


