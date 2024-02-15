




<h1 class="heading"><span class="name">MouseWheel</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Animation](./animation.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Form](./form.md) [Group](./group.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [MDIClient](./mdiclient.md) [ProgressBar](./progressbar.md) [PropertyPage](./propertypage.md) [RichEdit](./richedit.md) [Scroll](./scroll.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [ToolBar](./toolbar.md) [ToolControl](./toolcontrol.md) [TreeView](./treeview.md) | [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) | [Group](./group.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [MDIClient](./mdiclient.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [ToolBar](./toolbar.md) | [ToolControl](./toolcontrol.md) | [TreeView](./treeview.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) |
| [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) |
| [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) |
| [Edit](./edit.md) | [Form](./form.md) | [Group](./group.md) |
| [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) |
| [MDIClient](./mdiclient.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) |
| [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [Spinner](./spinner.md) |
| [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) |
| [TabBar](./tabbar.md) | [ToolBar](./toolbar.md) | [ToolControl](./toolcontrol.md) |
| [TreeView](./treeview.md) |  |  |


Description


If enabled, this event is reported when the user rotates the mouse wheel.


The event message reported as the result of `⎕DQ`,
or supplied as the right argument to your callback function, is a 9-element
vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'MouseWheel'` or 8 |
| `[3]` | Y | y-position of mouse (number) |
| `[4]` | X | x-position of mouse (number) |
| `[5]` | Button | button pressed 1 = left button 2 = right button 4 = middle button |
| `[6]` | Shift State | sum of shift key codes (number) 1 = Shift key is down 2 = Ctrl key is down |
| `[7]` | Delta | integer |
| `[8]` | Lines | integer |
| `[9]` | Wheel Delta | integer |


The value of *Delta* indicates the distance that the wheel is rotated,
expressed in multiples or divisions of *Wheel Delta*. A positive value
indicates that the wheel was rotated forward, away from the user; a negative
value indicates that the wheel was rotated backward, toward the user.


*Lines* specifies the number of lines to scroll when the wheel is
rotated by I *Mouse Delta* unit. A value of `¯1` indicates that a whole
screen is to be scrolled. These values are defined by the user's preferences (*Control
Panel/Mouse*).



