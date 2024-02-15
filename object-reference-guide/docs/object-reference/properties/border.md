




<h1 class="heading"><span class="name">Border</span></h1>

Applies To

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) [Animation](../a-z/animation.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Form](../a-z/form.md) [Grid](../a-z/grid.md) [Group](../a-z/group.md) [HTMLRenderer](../a-z/htmlrenderer.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [MDIClient](../a-z/mdiclient.md) [RichEdit](../a-z/richedit.md) [Scroll](../a-z/scroll.md) [SM](../a-z/sm.md) [Spinner](../a-z/spinner.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [StatusField](../a-z/statusfield.md) [SubForm](../a-z/subform.md) [TabBtn](../a-z/tabbtn.md) [ToolBar](../a-z/toolbar.md) [TrackBar](../a-z/trackbar.md) [TreeView](../a-z/treeview.md) [UpDown](../a-z/updown.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [HTMLRenderer](../a-z/htmlrenderer.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) | [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [StatusField](../a-z/statusfield.md) | [SubForm](../a-z/subform.md) | [TabBtn](../a-z/tabbtn.md) | [ToolBar](../a-z/toolbar.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) |
| [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [Combo](../a-z/combo.md) |
| [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) |
| [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) |
| [HTMLRenderer](../a-z/htmlrenderer.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) |
| [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) | [RichEdit](../a-z/richedit.md) |
| [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) |
| [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [StatusField](../a-z/statusfield.md) |
| [SubForm](../a-z/subform.md) | [TabBtn](../a-z/tabbtn.md) | [ToolBar](../a-z/toolbar.md) |
| [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |


Description


This property specifies whether or not an object is displayed with a border around it. It is a single number with the value 0 (no border)1 (Border), or 2. The value 2 applies only to a [Form](../a-z/form.md) and is used in combination with `('EdgeStyle' 'Dialog')` to obtain standard dialog box appearance


For a [Form](../a-z/form.md) or [SubForm](../a-z/subform.md), the value of the Border property is only relevant if [Sizeable](../a-z/sizeable.md), [Moveable](../a-z/moveable.md), [SysMenu](../a-z/sysmenu.md), [MaxButton](../a-z/maxbutton.md) and [MinButton](../a-z/minbutton.md) are all 0.

#### Note


The value of the Border property may only be assigned by `⎕WC` and may not be changed using `⎕WS`.



