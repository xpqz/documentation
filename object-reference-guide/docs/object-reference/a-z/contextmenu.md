




<h1 class="heading"><span class="name">ContextMenu</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Animation](./animation.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [CoolBar](./coolbar.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [MDIClient](./mdiclient.md) [ProgressBar](./progressbar.md) [PropertyPage](./propertypage.md) [RichEdit](./richedit.md) [Scroll](./scroll.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [ToolBar](./toolbar.md) [ToolControl](./toolcontrol.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [CoolBar](./coolbar.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [MDIClient](./mdiclient.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [ToolBar](./toolbar.md) | [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |  |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) |
| [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) |
| [Combo](./combo.md) | [ComboEx](./comboex.md) | [CoolBar](./coolbar.md) |
| [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) |
| [Grid](./grid.md) | [Group](./group.md) | [Label](./label.md) |
| [List](./list.md) | [ListView](./listview.md) | [MDIClient](./mdiclient.md) |
| [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [RichEdit](./richedit.md) |
| [Scroll](./scroll.md) | [Spinner](./spinner.md) | [Static](./static.md) |
| [StatusBar](./statusbar.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) |
| [ToolBar](./toolbar.md) | [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) |
| [TreeView](./treeview.md) | [UpDown](./updown.md) |  |


Description


If enabled, this event is reported when the user performs the standard
Windows action to display a ContextMenu. These include clicking/releasing the
right mouse button and pressing F10.



If the object has its own standard context menu, for example an Edit object,
the default action is to display this menu. If the object is dockable (see [Docking
Property](./dockable.md)), the default action is to display the standard (English) Dyalog
APL docking menu.


You may use this event to display your own pop-up context menu, by `⎕DQ`'ing
it within a callback function. In this case, your callback function should
return 0 to disable the standard context menu.



The event message reported as the result of `⎕DQ`,
or supplied as the right argument to your callback function, is a 5-element
vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'ContextMenu'` or 410 |
| `[3]` | (reserved) | Empty character vector |
| `[4]` | Y | y-position of the mouse (number) |
| `[5]` | X | x-position of the mouse (number) |



