




<h1 class="heading"><span class="name">Help</span></h1>

Applies To

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) [Animation](../a-z/animation.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [Circle](../a-z/circle.md) [ColorButton](../a-z/colorbutton.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [CoolBar](../a-z/coolbar.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Ellipse](../a-z/ellipse.md) [Form](../a-z/form.md) [Grid](../a-z/grid.md) [Group](../a-z/group.md) [Image](../a-z/image.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [Marker](../a-z/marker.md) [MDIClient](../a-z/mdiclient.md) [Poly](../a-z/poly.md) [ProgressBar](../a-z/progressbar.md) [PropertyPage](../a-z/propertypage.md) [Rect](../a-z/rect.md) [RichEdit](../a-z/richedit.md) [Scroll](../a-z/scroll.md) [SM](../a-z/sm.md) [Spinner](../a-z/spinner.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [SubForm](../a-z/subform.md) [TabBar](../a-z/tabbar.md) [Text](../a-z/text.md) [ToolBar](../a-z/toolbar.md) [ToolButton](../a-z/toolbutton.md) [ToolControl](../a-z/toolcontrol.md) [TrackBar](../a-z/trackbar.md) [TreeView](../a-z/treeview.md) [UpDown](../a-z/updown.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [Circle](../a-z/circle.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [CoolBar](../a-z/coolbar.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Ellipse](../a-z/ellipse.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [Image](../a-z/image.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [Marker](../a-z/marker.md) | [MDIClient](../a-z/mdiclient.md) | [Poly](../a-z/poly.md) | [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [Rect](../a-z/rect.md) | [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [Text](../a-z/text.md) | [ToolBar](../a-z/toolbar.md) | [ToolButton](../a-z/toolbutton.md) | [ToolControl](../a-z/toolcontrol.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |  |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) |
| [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [Circle](../a-z/circle.md) |
| [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) |
| [CoolBar](../a-z/coolbar.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) |
| [Ellipse](../a-z/ellipse.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) |
| [Group](../a-z/group.md) | [Image](../a-z/image.md) | [Label](../a-z/label.md) |
| [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [Marker](../a-z/marker.md) |
| [MDIClient](../a-z/mdiclient.md) | [Poly](../a-z/poly.md) | [ProgressBar](../a-z/progressbar.md) |
| [PropertyPage](../a-z/propertypage.md) | [Rect](../a-z/rect.md) | [RichEdit](../a-z/richedit.md) |
| [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) |
| [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) |
| [TabBar](../a-z/tabbar.md) | [Text](../a-z/text.md) | [ToolBar](../a-z/toolbar.md) |
| [ToolButton](../a-z/toolbutton.md) | [ToolControl](../a-z/toolcontrol.md) | [TrackBar](../a-z/trackbar.md) |
| [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |  |


Description


If enabled, this event is reported when the user clicks on an object which has a callback defined for this event, the user having previously clicked on the Question (?) button in the title bar of the parent Form.  The presence of the Question (?) button is determined by the value of the [HelpButton](../a-z/helpbutton.md) property.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 4-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'Help` or 400 |
| `[3]` | Y-coordinate | Number |
| `[4]` | X-coordinate | Number |


The y and x-coordinates refer to the position of the mouse pointer in the object which was clicked on, and are reported in the coordinate system of that object.



