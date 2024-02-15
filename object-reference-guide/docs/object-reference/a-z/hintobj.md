




<h1 class="heading"><span class="name">HintObj</span></h1>

Applies To

| Applies To: | [Animation](./animation.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [MDIClient](./mdiclient.md) [MenuItem](./menuitem.md) [ProgressBar](./progressbar.md) [PropertyPage](./propertypage.md) [PropertySheet](./propertysheet.md) [RichEdit](./richedit.md) [Root](./root.md) [Scroll](./scroll.md) [SM](./sm.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [ToolBar](./toolbar.md) [ToolButton](./toolbutton.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [MDIClient](./mdiclient.md) | [MenuItem](./menuitem.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) | [RichEdit](./richedit.md) | [Root](./root.md) | [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [ToolBar](./toolbar.md) | [ToolButton](./toolbutton.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |  |  |
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
| [ToolButton](./toolbutton.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) |
| [UpDown](./updown.md) |  |  |


Description


The HintObj property is a character vector or ref that specifies the name of, or a ref to, an object in which the "help" message defined by the Hint property is to be displayed. This message is displayed when the user positions the mouse pointer over the object. The Hint is displayed by automatically setting the Caption or Text property of the object named by HintObj.


The following types of object can therefore be used to display Hints: [Button](./button.md), [Edit](./edit.md), [Combo](./combo.md), [Group](./group.md), [Form](./form.md), [Label](./label.md), [Menu](./menu.md), [MenuItem](./menuitem.md), [StatusField](./statusfield.md), [SubForm](./subform.md) and [Text](./text.md). For a [StatusField](./statusfield.md) that has both Caption and Text properties, the text property is used for displaying hints.


When the user moves the mouse pointer away from the object, the Caption or Text property of the object specified by HintObj is reset to an empty vector.


Note that if HintObj is empty, its value is inherited from its parent. Thus setting HintObj on a [Form](./form.md) defines the default location for displaying Hints for all the controls in that [Form](./form.md). Setting HintObj on [Root](./root.md) defines the default location for hints for the entire application.



