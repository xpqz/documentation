




<h1 class="heading"><span class="name">TipObj</span></h1>

Applies To

| Applies To: | [Animation](./animation.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [MDIClient](./mdiclient.md) [MenuItem](./menuitem.md) [ProgressBar](./progressbar.md) [PropertyPage](./propertypage.md) [PropertySheet](./propertysheet.md) [RichEdit](./richedit.md) [Root](./root.md) [Scroll](./scroll.md) [SM](./sm.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [ToolBar](./toolbar.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [MDIClient](./mdiclient.md) | [MenuItem](./menuitem.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) | [RichEdit](./richedit.md) | [Root](./root.md) | [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [ToolBar](./toolbar.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |
| --- | --- | ---  |
| [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) |
| [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) |
| [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) |
| [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) |
| [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) |
| [MDIClient](./mdiclient.md) | [MenuItem](./menuitem.md) | [ProgressBar](./progressbar.md) |
| [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) | [RichEdit](./richedit.md) |
| [Root](./root.md) | [Scroll](./scroll.md) | [SM](./sm.md) |
| [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) |
| [SubForm](./subform.md) | [TabBar](./tabbar.md) | [ToolBar](./toolbar.md) |
| [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |


Description


The TipObj property is a character vector or ref that specifies the name of, or ref to, a [TipField](./tipfield.md) object in which the "help" message defined by the Tip property is to be displayed. This message is displayed when the user positions the mouse pointer over the object.


Note that if TipObj is empty, its value is inherited from its parent. Thus setting TipObj on a [Form](./form.md) defines the default [TipField](./tipfield.md) (and thus the default appearance of all Tips) for all the controls in that [Form](./form.md). Setting TipObj on [Root](./root.md) defines the default [TipField](./tipfield.md) for the entire application.



