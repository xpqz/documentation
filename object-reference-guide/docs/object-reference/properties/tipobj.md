




<h1 class="heading"><span class="name">TipObj</span></h1>

Applies To

| Applies To: | [Animation](../a-z/animation.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [ColorButton](../a-z/colorbutton.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Form](../a-z/form.md) [Grid](../a-z/grid.md) [Group](../a-z/group.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [MDIClient](../a-z/mdiclient.md) [MenuItem](../a-z/menuitem.md) [ProgressBar](../a-z/progressbar.md) [PropertyPage](../a-z/propertypage.md) [PropertySheet](../a-z/propertysheet.md) [RichEdit](../a-z/richedit.md) [Root](../a-z/root.md) [Scroll](../a-z/scroll.md) [SM](../a-z/sm.md) [Spinner](../a-z/spinner.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [SubForm](../a-z/subform.md) [TabBar](../a-z/tabbar.md) [ToolBar](../a-z/toolbar.md) [TrackBar](../a-z/trackbar.md) [TreeView](../a-z/treeview.md) [UpDown](../a-z/updown.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) | [MenuItem](../a-z/menuitem.md) | [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [PropertySheet](../a-z/propertysheet.md) | [RichEdit](../a-z/richedit.md) | [Root](../a-z/root.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [ToolBar](../a-z/toolbar.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |
| --- | --- | ---  |
| [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) |
| [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) |
| [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) |
| [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) |
| [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) |
| [MDIClient](../a-z/mdiclient.md) | [MenuItem](../a-z/menuitem.md) | [ProgressBar](../a-z/progressbar.md) |
| [PropertyPage](../a-z/propertypage.md) | [PropertySheet](../a-z/propertysheet.md) | [RichEdit](../a-z/richedit.md) |
| [Root](../a-z/root.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) |
| [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) |
| [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [ToolBar](../a-z/toolbar.md) |
| [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |


Description


The TipObj property is a character vector or ref that specifies the name of, or ref to, a [TipField](../a-z/tipfield.md) object in which the "help" message defined by the [Tip](../a-z/tip.md) property is to be displayed. This message is displayed when the user positions the mouse pointer over the object.


Note that if TipObj is empty, its value is inherited from its parent. Thus setting TipObj on a [Form](../a-z/form.md) defines the default [TipField](../a-z/tipfield.md) (and thus the default appearance of all [Tip](../a-z/tip.md)s) for all the controls in that [Form](../a-z/form.md). Setting TipObj on [Root](../a-z/root.md) defines the default [TipField](../a-z/tipfield.md) for the entire application.



