




<h1 class="heading"><span class="name">GotFocus</span></h1>

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


If enabled, this event is generated when the user has moved the keyboard focus to a new object by clicking the left mouse button, pressing TAB, or using a cursor key.




The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 3-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'GotFocus'` or 40 |
| `[3]` | Object name | character vector (name of object which previously had the focus) |



The third element (object name) is empty if the focus was obtained from another application window.


The GotFocus event is generated after the focus has changed. The default processing is therefore to take no action. However, if you disable the event by setting its action code to `¯1`, or inhibit it by returning a 0 from your callback function, the focus is automatically restored to the object (or external application) that had lost it.


