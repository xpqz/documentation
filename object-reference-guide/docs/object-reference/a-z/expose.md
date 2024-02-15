




<h1 class="heading"><span class="name">Expose</span></h1>

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


If enabled, this event is reported when part or all of the object's window is exposed to view. Under normal circumstances, APL repaints the exposed region automatically. However, if you have drawn unnamed graphical objects (which are not managed by APL) you should use this event to redraw them when required. Note that APL will itself repaint any named objects in the region before reporting the event.




The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 6-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'Expose'` or 32 |
| `[3]` | Y | y-position of top-left corner of exposed region |
| `[4]` | X | x-position of top-left corner of exposed region |
| `[5]` | H | height of exposed region |
| `[6]` | W | width of exposed region |


This event cannot be disabled by setting its action code to `¯1`. Similarly, setting the result of a callback function to 0 has no effect on it.



