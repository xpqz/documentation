




<h1 class="heading"><span class="name">TabIndex</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [MDIClient](./mdiclient.md) [ProgressBar](./progressbar.md) [RichEdit](./richedit.md) [Scroll](./scroll.md) [SM](./sm.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [ToolBar](./toolbar.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [ActiveXControl](./activexcontrol.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [MDIClient](./mdiclient.md) | [ProgressBar](./progressbar.md) | [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [ToolBar](./toolbar.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |  |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) |
| [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) |
| [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) |
| [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) |
| [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) |
| [MDIClient](./mdiclient.md) | [ProgressBar](./progressbar.md) | [RichEdit](./richedit.md) |
| [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) |
| [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) |
| [TabBar](./tabbar.md) | [ToolBar](./toolbar.md) | [TrackBar](./trackbar.md) |
| [TreeView](./treeview.md) | [UpDown](./updown.md) |  |


Description


The TabIndex property reports the `⎕IO`-dependent relative position of a child object within the list of child objects owned by its parent. If `N` is the number of children owned by an object, TabIndex is an integer between `⎕IO` and `(N-~⎕IO)`. The sequence of objects in this list is also used as the tabbing sequence, i.e. if the input focus is on the first child in the list, pressing Tab moves the input focus to the next child in the list.


When you create a child object, it is inserted in the list at the position specified by its TabIndex property. If TabIndex is omitted, it is appended to the end of the list.


If you subsequently change TabIndex, the object is moved to the corresponding position in the list.


Naturally, if you specify a value of TabIndex that is greater than the number of existing children, the object is inserted at or moved to the end of the list.



