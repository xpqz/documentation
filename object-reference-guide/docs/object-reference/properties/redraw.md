



<h1 class="heading"><span class="name">Redraw</span></h1>

Applies To

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [ColorButton](../a-z/colorbutton.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [CoolBar](../a-z/coolbar.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Form](../a-z/form.md) [Grid](../a-z/grid.md) [Group](../a-z/group.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [MDIClient](../a-z/mdiclient.md) [ProgressBar](../a-z/progressbar.md) [RichEdit](../a-z/richedit.md) [Scroll](../a-z/scroll.md) [SM](../a-z/sm.md) [Spinner](../a-z/spinner.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [SubForm](../a-z/subform.md) [TabBar](../a-z/tabbar.md) [ToolBar](../a-z/toolbar.md) [ToolControl](../a-z/toolcontrol.md) [TrackBar](../a-z/trackbar.md) [TreeView](../a-z/treeview.md) [UpDown](../a-z/updown.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [CoolBar](../a-z/coolbar.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) | [ProgressBar](../a-z/progressbar.md) | [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [ToolBar](../a-z/toolbar.md) | [ToolControl](../a-z/toolcontrol.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) |
| [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) |
| [ComboEx](../a-z/comboex.md) | [CoolBar](../a-z/coolbar.md) | [DateTimePicker](../a-z/datetimepicker.md) |
| [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) |
| [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) |
| [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) | [ProgressBar](../a-z/progressbar.md) |
| [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) |
| [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) |
| [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [ToolBar](../a-z/toolbar.md) |
| [ToolControl](../a-z/toolcontrol.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) |
| [UpDown](../a-z/updown.md) |  |  |


Description


The Redraw property specifies whether or not APL automatically redraws an object when it is exposed or when any of its properties change in a way that would affect its appearance.


The value reported by the Redraw property is a Boolean value; 1 means that APL automatically redraws the object when necessary (the default); 0 means that APL does not redraw the object.


Setting Redraw to 0 or 1 affects only whether or not APL will redraw the object from then on.


Setting Redraw to 2 has the same effect as setting it to 1, but the object is also redrawn immediately. Note that no child object is redrawn.


Setting Redraw to 3 has the same effect as setting it to 1, but the object and its children are redrawn immediately.


