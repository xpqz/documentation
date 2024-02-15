




<h1 class="heading"><span class="name">MouseDblClick</span></h1>

Applies To

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) [Animation](../a-z/animation.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [Circle](../a-z/circle.md) [ColorButton](../a-z/colorbutton.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Ellipse](../a-z/ellipse.md) [Form](../a-z/form.md) [Group](../a-z/group.md) [Image](../a-z/image.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [Marker](../a-z/marker.md) [MDIClient](../a-z/mdiclient.md) [Poly](../a-z/poly.md) [ProgressBar](../a-z/progressbar.md) [PropertyPage](../a-z/propertypage.md) [Rect](../a-z/rect.md) [RichEdit](../a-z/richedit.md) [Scroll](../a-z/scroll.md) [SM](../a-z/sm.md) [Spinner](../a-z/spinner.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [StatusField](../a-z/statusfield.md) [SubForm](../a-z/subform.md) [SysTrayItem](../a-z/systrayitem.md) [TabBar](../a-z/tabbar.md) [TabBtn](../a-z/tabbtn.md) [Text](../a-z/text.md) [ToolBar](../a-z/toolbar.md) [ToolButton](../a-z/toolbutton.md) [ToolControl](../a-z/toolcontrol.md) [TreeView](../a-z/treeview.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [Circle](../a-z/circle.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Ellipse](../a-z/ellipse.md) | [Form](../a-z/form.md) | [Group](../a-z/group.md) | [Image](../a-z/image.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [Marker](../a-z/marker.md) | [MDIClient](../a-z/mdiclient.md) | [Poly](../a-z/poly.md) | [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [Rect](../a-z/rect.md) | [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [StatusField](../a-z/statusfield.md) | [SubForm](../a-z/subform.md) | [SysTrayItem](../a-z/systrayitem.md) | [TabBar](../a-z/tabbar.md) | [TabBtn](../a-z/tabbtn.md) | [Text](../a-z/text.md) | [ToolBar](../a-z/toolbar.md) | [ToolButton](../a-z/toolbutton.md) | [ToolControl](../a-z/toolcontrol.md) | [TreeView](../a-z/treeview.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) |
| [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [Circle](../a-z/circle.md) |
| [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) |
| [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Ellipse](../a-z/ellipse.md) |
| [Form](../a-z/form.md) | [Group](../a-z/group.md) | [Image](../a-z/image.md) |
| [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) |
| [Marker](../a-z/marker.md) | [MDIClient](../a-z/mdiclient.md) | [Poly](../a-z/poly.md) |
| [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [Rect](../a-z/rect.md) |
| [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) |
| [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) |
| [StatusField](../a-z/statusfield.md) | [SubForm](../a-z/subform.md) | [SysTrayItem](../a-z/systrayitem.md) |
| [TabBar](../a-z/tabbar.md) | [TabBtn](../a-z/tabbtn.md) | [Text](../a-z/text.md) |
| [ToolBar](../a-z/toolbar.md) | [ToolButton](../a-z/toolbutton.md) | [ToolControl](../a-z/toolcontrol.md) |
| [TreeView](../a-z/treeview.md) |  |  |


Description


If enabled, this event is reported when the user presses and then releases a mouse button twice within a short space of time. The duration of this time is set through the Windows Control Panel.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 6-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'MouseDblClick'` or 5 |
| `[3]` | Y | y-position of mouse (number) |
| `[4]` | X | x-position of mouse (number) |
| `[5]` | Button | button double clicked (number) 1 = left button 2 = right button 4 = middle button |
| `[6]` | Shift State | sum of shift key codes (number) 1 = Shift key is down 2 = Ctrl key is down |


In a graphical object ([Circle](../a-z/circle.md), [Ellipse](../a-z/ellipse.md), [Image](../a-z/image.md), [Marker](../a-z/marker.md), [Poly](../a-z/poly.md) and [Rect](../a-z/rect.md)), the position of the mouse is reported relative to the top-left corner of its bounding rectangle.


If you enable [MouseDown](../a-z/mousedown.md) and [MouseUp](../a-z/mouseup.md) events in addition to MouseDblClick events, double-clicking a mouse button will generate the following sequence of events :

1. [MouseDown](../a-z/mousedown.md)

2. [MouseUp](../a-z/mouseup.md)

3. MouseDblClick
4. [MouseUp](../a-z/mouseup.md)



