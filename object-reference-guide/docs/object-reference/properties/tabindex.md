




<h1 class="heading"><span class="name">TabIndex</span></h1>

Applies To

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [ColorButton](../a-z/colorbutton.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Form](../a-z/form.md) [Grid](../a-z/grid.md) [Group](../a-z/group.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [MDIClient](../a-z/mdiclient.md) [ProgressBar](../a-z/progressbar.md) [RichEdit](../a-z/richedit.md) [Scroll](../a-z/scroll.md) [SM](../a-z/sm.md) [Spinner](../a-z/spinner.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [SubForm](../a-z/subform.md) [TabBar](../a-z/tabbar.md) [ToolBar](../a-z/toolbar.md) [TrackBar](../a-z/trackbar.md) [TreeView](../a-z/treeview.md) [UpDown](../a-z/updown.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) | [ProgressBar](../a-z/progressbar.md) | [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [ToolBar](../a-z/toolbar.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |  |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) |
| [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) |
| [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) |
| [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) |
| [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) |
| [MDIClient](../a-z/mdiclient.md) | [ProgressBar](../a-z/progressbar.md) | [RichEdit](../a-z/richedit.md) |
| [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) |
| [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) |
| [TabBar](../a-z/tabbar.md) | [ToolBar](../a-z/toolbar.md) | [TrackBar](../a-z/trackbar.md) |
| [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |  |


Description


The TabIndex property reports the `⎕IO`-dependent relative position of a child object within the list of child objects owned by its parent. If `N` is the number of children owned by an object, TabIndex is an integer between `⎕IO` and `(N-~⎕IO)`. The sequence of objects in this list is also used as the tabbing sequence, i.e. if the input focus is on the first child in the list, pressing Tab moves the input focus to the next child in the list.


When you create a child object, it is inserted in the list at the position specified by its TabIndex property. If TabIndex is omitted, it is appended to the end of the list.


If you subsequently change TabIndex, the object is moved to the corresponding position in the list.


Naturally, if you specify a value of TabIndex that is greater than the number of existing children, the object is inserted at or moved to the end of the list.



