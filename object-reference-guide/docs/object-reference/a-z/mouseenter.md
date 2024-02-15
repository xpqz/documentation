




<h1 class="heading"><span class="name">MouseEnter</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Animation](./animation.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [MDIClient](./mdiclient.md) [ProgressBar](./progressbar.md) [PropertyPage](./propertypage.md) [RichEdit](./richedit.md) [Scroll](./scroll.md) [SM](./sm.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [ToolBar](./toolbar.md) [ToolControl](./toolcontrol.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [MDIClient](./mdiclient.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [ToolBar](./toolbar.md) | [ToolControl](./toolcontrol.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) |
| [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) |
| [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) |
| [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) |
| [Group](./group.md) | [Label](./label.md) | [List](./list.md) |
| [ListView](./listview.md) | [MDIClient](./mdiclient.md) | [ProgressBar](./progressbar.md) |
| [PropertyPage](./propertypage.md) | [RichEdit](./richedit.md) | [Scroll](./scroll.md) |
| [SM](./sm.md) | [Spinner](./spinner.md) | [Static](./static.md) |
| [StatusBar](./statusbar.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) |
| [ToolBar](./toolbar.md) | [ToolControl](./toolcontrol.md) | [TreeView](./treeview.md) |
| [UpDown](./updown.md) |  |  |


Description


If enabled, this event is reported when the user moves the mouse pointer into (over) an object. The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 3-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'MouseEnter'` or 6 |
| `[3]` | Object name | character vector (name of previous object) |


This event is generated when the user moves the mouse pointer across the boundary and into an object. The first element of the event message is the name of the object over which the mouse pointer now resides. The 3rd element of the event message contains the name of the object that was previously under the mouse pointer, or is an empty vector if the mouse pointer was not previously over a Dyalog APL/W object.



