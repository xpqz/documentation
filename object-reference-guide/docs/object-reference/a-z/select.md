




<h1 class="heading"><span class="name">Select</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Bitmap](./bitmap.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [Circle](./circle.md) [Clipboard](./clipboard.md) [Combo](./combo.md) [ComboEx](./comboex.md) [Cursor](./cursor.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Ellipse](./ellipse.md) [FileBox](./filebox.md) [Font](./font.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [Icon](./icon.md) [Image](./image.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [Locator](./locator.md) [Marker](./marker.md) [MDIClient](./mdiclient.md) [Menu](./menu.md) [MenuItem](./menuitem.md) [Metafile](./metafile.md) [Poly](./poly.md) [Printer](./printer.md) [ProgressBar](./progressbar.md) [Rect](./rect.md) [RichEdit](./richedit.md) [Scroll](./scroll.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [StatusField](./statusfield.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [TabBtn](./tabbtn.md) [TabButton](./tabbutton.md) [Text](./text.md) [ToolBar](./toolbar.md) [ToolButton](./toolbutton.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [ActiveXControl](./activexcontrol.md) | [Bitmap](./bitmap.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [Circle](./circle.md) | [Clipboard](./clipboard.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [Cursor](./cursor.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Ellipse](./ellipse.md) | [FileBox](./filebox.md) | [Font](./font.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [Icon](./icon.md) | [Image](./image.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [Locator](./locator.md) | [Marker](./marker.md) | [MDIClient](./mdiclient.md) | [Menu](./menu.md) | [MenuItem](./menuitem.md) | [Metafile](./metafile.md) | [Poly](./poly.md) | [Printer](./printer.md) | [ProgressBar](./progressbar.md) | [Rect](./rect.md) | [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) | [TabButton](./tabbutton.md) | [Text](./text.md) | [ToolBar](./toolbar.md) | [ToolButton](./toolbutton.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Bitmap](./bitmap.md) | [Button](./button.md) |
| [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [Circle](./circle.md) |
| [Clipboard](./clipboard.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) |
| [Cursor](./cursor.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) |
| [Ellipse](./ellipse.md) | [FileBox](./filebox.md) | [Font](./font.md) |
| [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) |
| [Icon](./icon.md) | [Image](./image.md) | [Label](./label.md) |
| [List](./list.md) | [ListView](./listview.md) | [Locator](./locator.md) |
| [Marker](./marker.md) | [MDIClient](./mdiclient.md) | [Menu](./menu.md) |
| [MenuItem](./menuitem.md) | [Metafile](./metafile.md) | [Poly](./poly.md) |
| [Printer](./printer.md) | [ProgressBar](./progressbar.md) | [Rect](./rect.md) |
| [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [Spinner](./spinner.md) |
| [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) |
| [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) |
| [TabButton](./tabbutton.md) | [Text](./text.md) | [ToolBar](./toolbar.md) |
| [ToolButton](./toolbutton.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) |
| [UpDown](./updown.md) |  |  |



Description


For a [Button](./button.md) with [Style](./style.md)`'Push'` this event is generated when the user "pushes" the button. This can be done by clicking the left mouse button, or by pressing the Enter key or the space bar when the [Button](./button.md) has the focus. The Select event can also be generated when the [Button](./button.md) does not have the focus, by pressing the Enter key when its [Default](./default.md) property is 1 or by pressing the ESC key when its [Cancel](./cancel.md) property is 1.


For a [Button](./button.md) with [Style](./style.md)`'Radio'` or `'Check'` this event is generated when the user toggles the button from one state to another. This can be achieved by clicking the left mouse button or by pressing the space bar when the [Button](./button.md) has the focus.


For a [Combo](./combo.md) or [List](./list.md) object, a Select event is generated when the user selects an item from the list, whether by pressing the arrow keys or by clicking the left mouse button.


For a [MenuItem](./menuitem.md), a Select event is generated when the user chooses the item.


For all other objects, this event is generated when the user presses the keys associated with the object's [Accelerator](./accelerator.md) property.



The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | Event code |



