




<h1 class="heading"><span class="name">Help</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Animation](./animation.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [Circle](./circle.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [CoolBar](./coolbar.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Ellipse](./ellipse.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [Image](./image.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [Marker](./marker.md) [MDIClient](./mdiclient.md) [Poly](./poly.md) [ProgressBar](./progressbar.md) [PropertyPage](./propertypage.md) [Rect](./rect.md) [RichEdit](./richedit.md) [Scroll](./scroll.md) [SM](./sm.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [Text](./text.md) [ToolBar](./toolbar.md) [ToolButton](./toolbutton.md) [ToolControl](./toolcontrol.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [Circle](./circle.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [CoolBar](./coolbar.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Ellipse](./ellipse.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [Image](./image.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [Marker](./marker.md) | [MDIClient](./mdiclient.md) | [Poly](./poly.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [Rect](./rect.md) | [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [Text](./text.md) | [ToolBar](./toolbar.md) | [ToolButton](./toolbutton.md) | [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |  |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) |
| [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [Circle](./circle.md) |
| [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) |
| [CoolBar](./coolbar.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) |
| [Ellipse](./ellipse.md) | [Form](./form.md) | [Grid](./grid.md) |
| [Group](./group.md) | [Image](./image.md) | [Label](./label.md) |
| [List](./list.md) | [ListView](./listview.md) | [Marker](./marker.md) |
| [MDIClient](./mdiclient.md) | [Poly](./poly.md) | [ProgressBar](./progressbar.md) |
| [PropertyPage](./propertypage.md) | [Rect](./rect.md) | [RichEdit](./richedit.md) |
| [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) |
| [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) |
| [TabBar](./tabbar.md) | [Text](./text.md) | [ToolBar](./toolbar.md) |
| [ToolButton](./toolbutton.md) | [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) |
| [TreeView](./treeview.md) | [UpDown](./updown.md) |  |


Description


If enabled, this event is reported when the user clicks on an object which has a callback defined for this event, the user having previously clicked on the Question (?) button in the title bar of the parent Form.  The presence of the Question (?) button is determined by the value of the [HelpButton](./helpbutton.md) property.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 4-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'Help` or 400 |
| `[3]` | Y-coordinate | Number |
| `[4]` | X-coordinate | Number |


The y and x-coordinates refer to the position of the mouse pointer in the object which was clicked on, and are reported in the coordinate system of that object.



