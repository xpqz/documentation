




<h1 class="heading"><span class="name">Active</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Animation](./animation.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [Menu](./menu.md) [MenuItem](./menuitem.md) [ProgressBar](./progressbar.md) [PropertyPage](./propertypage.md) [PropertySheet](./propertysheet.md) [RichEdit](./richedit.md) [Scroll](./scroll.md) [Spinner](./spinner.md) [Splitter](./splitter.md) [Static](./static.md) [StatusBar](./statusbar.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [TabBtn](./tabbtn.md) [Text](./text.md) [Timer](./timer.md) [ToolBar](./toolbar.md) [ToolButton](./toolbutton.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [Menu](./menu.md) | [MenuItem](./menuitem.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) | [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [Spinner](./spinner.md) | [Splitter](./splitter.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) | [Text](./text.md) | [Timer](./timer.md) | [ToolBar](./toolbar.md) | [ToolButton](./toolbutton.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) |
| [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) |
| [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) |
| [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) |
| [Group](./group.md) | [Label](./label.md) | [List](./list.md) |
| [ListView](./listview.md) | [Menu](./menu.md) | [MenuItem](./menuitem.md) |
| [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) |
| [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [Spinner](./spinner.md) |
| [Splitter](./splitter.md) | [Static](./static.md) | [StatusBar](./statusbar.md) |
| [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) |
| [Text](./text.md) | [Timer](./timer.md) | [ToolBar](./toolbar.md) |
| [ToolButton](./toolbutton.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) |
| [UpDown](./updown.md) |  |  |


Description


This property specifies whether or not an object is currently responsive to user actions. It is a single number with the value 0 (object is inactive and does not generate events) or 1 (object is active and capable of generating events). The default is 1.


Setting Active to 0 disables the object (and all its children), even though the object may be referenced in the argument to `⎕DQ`. It is therefore possible to deactivate an object from a callback function.


In general, the text associated with an object whose Active property is 0 is displayed in grey.



