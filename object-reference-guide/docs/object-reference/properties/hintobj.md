




<h1 class="heading"><span class="name">HintObj</span></h1>

Applies To

| Applies To: | [Animation](../a-z/animation.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [ColorButton](../a-z/colorbutton.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Form](../a-z/form.md) [Grid](../a-z/grid.md) [Group](../a-z/group.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [MDIClient](../a-z/mdiclient.md) [MenuItem](../a-z/menuitem.md) [ProgressBar](../a-z/progressbar.md) [PropertyPage](../a-z/propertypage.md) [PropertySheet](../a-z/propertysheet.md) [RichEdit](../a-z/richedit.md) [Root](../a-z/root.md) [Scroll](../a-z/scroll.md) [SM](../a-z/sm.md) [Spinner](../a-z/spinner.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [SubForm](../a-z/subform.md) [TabBar](../a-z/tabbar.md) [ToolBar](../a-z/toolbar.md) [ToolButton](../a-z/toolbutton.md) [TrackBar](../a-z/trackbar.md) [TreeView](../a-z/treeview.md) [UpDown](../a-z/updown.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) | [MenuItem](../a-z/menuitem.md) | [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [PropertySheet](../a-z/propertysheet.md) | [RichEdit](../a-z/richedit.md) | [Root](../a-z/root.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [ToolBar](../a-z/toolbar.md) | [ToolButton](../a-z/toolbutton.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |  |  |
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
| [ToolButton](../a-z/toolbutton.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) |
| [UpDown](../a-z/updown.md) |  |  |


Description


The HintObj property is a character vector or ref that specifies the name of, or a ref to, an object in which the "help" message defined by the [Hint](../a-z/hint.md) property is to be displayed. This message is displayed when the user positions the mouse pointer over the object. The [Hint](../a-z/hint.md) is displayed by automatically setting the [Caption](../a-z/caption.md) or [Text](../a-z/text.md) property of the object named by HintObj.


The following types of object can therefore be used to display Hints: [Button](../a-z/button.md), [Edit](../a-z/edit.md), [Combo](../a-z/combo.md), [Group](../a-z/group.md), [Form](../a-z/form.md), [Label](../a-z/label.md), [Menu](../a-z/menu.md), [MenuItem](../a-z/menuitem.md), [StatusField](../a-z/statusfield.md), [SubForm](../a-z/subform.md) and [Text](../a-z/text.md). For a [StatusField](../a-z/statusfield.md) that has both [Caption](../a-z/caption.md) and [Text](../a-z/text.md) properties, the text property is used for displaying hints.


When the user moves the mouse pointer away from the object, the [Caption](../a-z/caption.md) or [Text](../a-z/text.md) property of the object specified by HintObj is reset to an empty vector.


Note that if HintObj is empty, its value is inherited from its parent. Thus setting HintObj on a [Form](../a-z/form.md) defines the default location for displaying [Hint](../a-z/hint.md)s for all the controls in that [Form](../a-z/form.md). Setting HintObj on [Root](../a-z/root.md) defines the default location for hints for the entire application.



