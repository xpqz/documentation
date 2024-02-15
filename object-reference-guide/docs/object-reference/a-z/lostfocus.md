




<h1 class="heading"><span class="name">LostFocus</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Animation](./animation.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [List](./list.md) [ListView](./listview.md) [MDIClient](./mdiclient.md) [ProgressBar](./progressbar.md) [PropertyPage](./propertypage.md) [RichEdit](./richedit.md) [Scroll](./scroll.md) [Spinner](./spinner.md) [SubForm](./subform.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) | [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [List](./list.md) | [ListView](./listview.md) | [MDIClient](./mdiclient.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [Spinner](./spinner.md) | [SubForm](./subform.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) |
| [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) |
| [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) |
| [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) |
| [Group](./group.md) | [List](./list.md) | [ListView](./listview.md) |
| [MDIClient](./mdiclient.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) |
| [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [Spinner](./spinner.md) |
| [SubForm](./subform.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) |


Description


If enabled, this event is generated when the user transfers the keyboard focus away from the object in question.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 3-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'LostFocus'` or 41 |
| `[3]` | Object name | character vector (name of object that has received the focus) |


If the focus is transferred to a window that is not part of the Dyalog APL GUI Interface, the third element is an empty vector.


The LostFocus event is generated after the focus has changed. The default processing is therefore to take no action. However, if you inhibit the event by returning a 0 from your callback function, the focus is automatically restored to the object that had lost it.



