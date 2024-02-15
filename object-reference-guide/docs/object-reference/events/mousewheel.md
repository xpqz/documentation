




<h1 class="heading"><span class="name">MouseWheel</span></h1>

Applies To

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) [Animation](../a-z/animation.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [ColorButton](../a-z/colorbutton.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Form](../a-z/form.md) [Group](../a-z/group.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [MDIClient](../a-z/mdiclient.md) [ProgressBar](../a-z/progressbar.md) [PropertyPage](../a-z/propertypage.md) [RichEdit](../a-z/richedit.md) [Scroll](../a-z/scroll.md) [Spinner](../a-z/spinner.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [SubForm](../a-z/subform.md) [TabBar](../a-z/tabbar.md) [ToolBar](../a-z/toolbar.md) [ToolControl](../a-z/toolcontrol.md) [TreeView](../a-z/treeview.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) | [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [ToolBar](../a-z/toolbar.md) | [ToolControl](../a-z/toolcontrol.md) | [TreeView](../a-z/treeview.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) |
| [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) |
| [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) |
| [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Group](../a-z/group.md) |
| [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) |
| [MDIClient](../a-z/mdiclient.md) | [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) |
| [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [Spinner](../a-z/spinner.md) |
| [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) |
| [TabBar](../a-z/tabbar.md) | [ToolBar](../a-z/toolbar.md) | [ToolControl](../a-z/toolcontrol.md) |
| [TreeView](../a-z/treeview.md) |  |  |


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



