




<h1 class="heading"><span class="name">DropFiles</span></h1>

Applies To

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) [Animation](../a-z/animation.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [ColorButton](../a-z/colorbutton.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [CoolBar](../a-z/coolbar.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Form](../a-z/form.md) [Grid](../a-z/grid.md) [Group](../a-z/group.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [MDIClient](../a-z/mdiclient.md) [ProgressBar](../a-z/progressbar.md) [PropertyPage](../a-z/propertypage.md) [RichEdit](../a-z/richedit.md) [Scroll](../a-z/scroll.md) [Spinner](../a-z/spinner.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [SubForm](../a-z/subform.md) [TabBar](../a-z/tabbar.md) [ToolBar](../a-z/toolbar.md) [ToolControl](../a-z/toolcontrol.md) [TrackBar](../a-z/trackbar.md) [TreeView](../a-z/treeview.md) [UpDown](../a-z/updown.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [CoolBar](../a-z/coolbar.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) | [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [ToolBar](../a-z/toolbar.md) | [ToolControl](../a-z/toolcontrol.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |  |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) |
| [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) |
| [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [CoolBar](../a-z/coolbar.md) |
| [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) |
| [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [Label](../a-z/label.md) |
| [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) |
| [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [RichEdit](../a-z/richedit.md) |
| [Scroll](../a-z/scroll.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) |
| [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) |
| [ToolBar](../a-z/toolbar.md) | [ToolControl](../a-z/toolcontrol.md) | [TrackBar](../a-z/trackbar.md) |
| [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |  |


Description


If enabled, this event is reported when the user drags a file icon or a set of file icons and drops them onto the object. The system takes no action other than to report the event.


Note that the event is only reported if [AcceptFiles](../a-z/acceptfiles.md) is set to 1.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 5-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'DropFiles'` or 450 |
| `[3]` | Files | Vector of character vectors containing the file names. |
| `[4]` | Item number | Integer. The index of the item within the object onto which the file(s) was dropped. Applies only to objects that have an [Items](../a-z/items.md) property such as List, [ListView](../a-z/listview.md) and [TreeView](../a-z/treeview.md) . |
| `[5]` | Shift state | Integer. Sum of 1=shift key, 2=Ctrl key, 4=Alt key |



