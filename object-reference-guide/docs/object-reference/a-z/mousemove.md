




<h1 class="heading"><span class="name">MouseMove</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Animation](./animation.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [Circle](./circle.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Ellipse](./ellipse.md) [Form](./form.md) [Group](./group.md) [Image](./image.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [Marker](./marker.md) [MDIClient](./mdiclient.md) [Poly](./poly.md) [ProgressBar](./progressbar.md) [PropertyPage](./propertypage.md) [Rect](./rect.md) [RichEdit](./richedit.md) [Scroll](./scroll.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [StatusField](./statusfield.md) [SubForm](./subform.md) [SysTrayItem](./systrayitem.md) [TabBar](./tabbar.md) [TabBtn](./tabbtn.md) [Text](./text.md) [ToolBar](./toolbar.md) [ToolButton](./toolbutton.md) [ToolControl](./toolcontrol.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [Circle](./circle.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Ellipse](./ellipse.md) | [Form](./form.md) | [Group](./group.md) | [Image](./image.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [Marker](./marker.md) | [MDIClient](./mdiclient.md) | [Poly](./poly.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [Rect](./rect.md) | [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) | [SubForm](./subform.md) | [SysTrayItem](./systrayitem.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) | [Text](./text.md) | [ToolBar](./toolbar.md) | [ToolButton](./toolbutton.md) | [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |  |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) |
| [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [Circle](./circle.md) |
| [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) |
| [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Ellipse](./ellipse.md) |
| [Form](./form.md) | [Group](./group.md) | [Image](./image.md) |
| [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) |
| [Marker](./marker.md) | [MDIClient](./mdiclient.md) | [Poly](./poly.md) |
| [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [Rect](./rect.md) |
| [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [Spinner](./spinner.md) |
| [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) |
| [SubForm](./subform.md) | [SysTrayItem](./systrayitem.md) | [TabBar](./tabbar.md) |
| [TabBtn](./tabbtn.md) | [Text](./text.md) | [ToolBar](./toolbar.md) |
| [ToolButton](./toolbutton.md) | [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) |
| [TreeView](./treeview.md) | [UpDown](./updown.md) |  |


Description


If enabled, this event is reported when the user moves the mouse. The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 6-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'MouseMove'` or 3 |
| `[3]` | Y | y-position of mouse (number) |
| `[4]` | X | x-position of mouse (number) |
| `[5]` | Button | button released (number) 1 = left button 2 = right button 4 = middle button |
| `[6]` | Shift State | sum of shift key codes (number) 1 = Shift key is down 2 = Ctrl key is down |


In a graphical object ([Circle](./circle.md), [Ellipse](./ellipse.md), [Image](./image.md), [Marker](./marker.md), [Poly](./poly.md) and [Rect](./rect.md)), the position of the mouse is reported relative to the top-left corner of its bounding rectangle.


Note that rapid movement of the mouse will not necessarily cause an overwhelming number of MouseMove events to be reported, as several small movements are automatically combined into one large one.



