




<h1 class="heading"><span class="name">Active</span></h1>

Applies To

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) [Animation](../a-z/animation.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [ColorButton](../a-z/colorbutton.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Form](../a-z/form.md) [Grid](../a-z/grid.md) [Group](../a-z/group.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [Menu](../a-z/menu.md) [MenuItem](../a-z/menuitem.md) [ProgressBar](../a-z/progressbar.md) [PropertyPage](../a-z/propertypage.md) [PropertySheet](../a-z/propertysheet.md) [RichEdit](../a-z/richedit.md) [Scroll](../a-z/scroll.md) [Spinner](../a-z/spinner.md) [Splitter](../a-z/splitter.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [SubForm](../a-z/subform.md) [TabBar](../a-z/tabbar.md) [TabBtn](../a-z/tabbtn.md) [Text](../a-z/text.md) [Timer](../a-z/timer.md) [ToolBar](../a-z/toolbar.md) [ToolButton](../a-z/toolbutton.md) [TrackBar](../a-z/trackbar.md) [TreeView](../a-z/treeview.md) [UpDown](../a-z/updown.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [Menu](../a-z/menu.md) | [MenuItem](../a-z/menuitem.md) | [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [PropertySheet](../a-z/propertysheet.md) | [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [Spinner](../a-z/spinner.md) | [Splitter](../a-z/splitter.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [TabBtn](../a-z/tabbtn.md) | [Text](../a-z/text.md) | [Timer](../a-z/timer.md) | [ToolBar](../a-z/toolbar.md) | [ToolButton](../a-z/toolbutton.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) |
| [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) |
| [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) |
| [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) |
| [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) |
| [ListView](../a-z/listview.md) | [Menu](../a-z/menu.md) | [MenuItem](../a-z/menuitem.md) |
| [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [PropertySheet](../a-z/propertysheet.md) |
| [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [Spinner](../a-z/spinner.md) |
| [Splitter](../a-z/splitter.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) |
| [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [TabBtn](../a-z/tabbtn.md) |
| [Text](../a-z/text.md) | [Timer](../a-z/timer.md) | [ToolBar](../a-z/toolbar.md) |
| [ToolButton](../a-z/toolbutton.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) |
| [UpDown](../a-z/updown.md) |  |  |


Description


This property specifies whether or not an object is currently responsive to user actions. It is a single number with the value 0 (object is inactive and does not generate events) or 1 (object is active and capable of generating events). The default is 1.


Setting Active to 0 disables the object (and all its children), even though the object may be referenced in the argument to `⎕DQ`. It is therefore possible to deactivate an object from a callback function.


In general, the text associated with an object whose Active property is 0 is displayed in grey.



