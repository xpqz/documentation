




<h1 class="heading"><span class="name">MouseEnter</span></h1>

Applies To

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) [Animation](../a-z/animation.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [ColorButton](../a-z/colorbutton.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Form](../a-z/form.md) [Grid](../a-z/grid.md) [Group](../a-z/group.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [MDIClient](../a-z/mdiclient.md) [ProgressBar](../a-z/progressbar.md) [PropertyPage](../a-z/propertypage.md) [RichEdit](../a-z/richedit.md) [Scroll](../a-z/scroll.md) [SM](../a-z/sm.md) [Spinner](../a-z/spinner.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [SubForm](../a-z/subform.md) [TabBar](../a-z/tabbar.md) [ToolBar](../a-z/toolbar.md) [ToolControl](../a-z/toolcontrol.md) [TreeView](../a-z/treeview.md) [UpDown](../a-z/updown.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) | [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [ToolBar](../a-z/toolbar.md) | [ToolControl](../a-z/toolcontrol.md) | [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) |
| [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) |
| [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) |
| [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) |
| [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) |
| [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) | [ProgressBar](../a-z/progressbar.md) |
| [PropertyPage](../a-z/propertypage.md) | [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) |
| [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) |
| [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) |
| [ToolBar](../a-z/toolbar.md) | [ToolControl](../a-z/toolcontrol.md) | [TreeView](../a-z/treeview.md) |
| [UpDown](../a-z/updown.md) |  |  |


Description


If enabled, this event is reported when the user moves the mouse pointer into (over) an object. The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 3-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'MouseEnter'` or 6 |
| `[3]` | Object name | character vector (name of previous object) |


This event is generated when the user moves the mouse pointer across the boundary and into an object. The first element of the event message is the name of the object over which the mouse pointer now resides. The 3rd element of the event message contains the name of the object that was previously under the mouse pointer, or is an empty vector if the mouse pointer was not previously over a Dyalog APL/W object.



