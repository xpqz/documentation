




<h1 class="heading"><span class="name">GotFocus</span></h1>

Applies To

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) [Animation](../a-z/animation.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [ColorButton](../a-z/colorbutton.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Form](../a-z/form.md) [Grid](../a-z/grid.md) [Group](../a-z/group.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [MDIClient](../a-z/mdiclient.md) [ProgressBar](../a-z/progressbar.md) [PropertyPage](../a-z/propertypage.md) [RichEdit](../a-z/richedit.md) [Scroll](../a-z/scroll.md) [Spinner](../a-z/spinner.md) [SubForm](../a-z/subform.md) [TrackBar](../a-z/trackbar.md) [TreeView](../a-z/treeview.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) | [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [Spinner](../a-z/spinner.md) | [SubForm](../a-z/subform.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) |
| [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) |
| [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) |
| [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) |
| [Group](../a-z/group.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) |
| [MDIClient](../a-z/mdiclient.md) | [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) |
| [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [Spinner](../a-z/spinner.md) |
| [SubForm](../a-z/subform.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) |


Description


If enabled, this event is generated when the user has moved the keyboard focus to a new object by clicking the left mouse button, pressing TAB, or using a cursor key.




The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 3-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'GotFocus'` or 40 |
| `[3]` | Object name | character vector (name of object which previously had the focus) |



The third element (object name) is empty if the focus was obtained from another application window.


The GotFocus event is generated after the focus has changed. The default processing is therefore to take no action. However, if you disable the event by setting its action code to `¯1`, or inhibit it by returning a 0 from your callback function, the focus is automatically restored to the object (or external application) that had lost it.


