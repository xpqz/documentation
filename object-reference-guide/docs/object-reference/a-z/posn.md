




<h1 class="heading"><span class="name">Posn</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Animation](./animation.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [CoolBand](./coolband.md) [CoolBar](./coolbar.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [HTMLRenderer](./htmlrenderer.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [Locator](./locator.md) [MDIClient](./mdiclient.md) [Menu](./menu.md) [MenuItem](./menuitem.md) [ProgressBar](./progressbar.md) [PropertyPage](./propertypage.md) [PropertySheet](./propertysheet.md) [RichEdit](./richedit.md) [Root](./root.md) [Scroll](./scroll.md) [Separator](./separator.md) [SM](./sm.md) [Spinner](./spinner.md) [Splitter](./splitter.md) [Static](./static.md) [StatusBar](./statusbar.md) [StatusField](./statusfield.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [TabBtn](./tabbtn.md) [TabButton](./tabbutton.md) [TabControl](./tabcontrol.md) [ToolBar](./toolbar.md) [ToolButton](./toolbutton.md) [ToolControl](./toolcontrol.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [CoolBand](./coolband.md) | [CoolBar](./coolbar.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [HTMLRenderer](./htmlrenderer.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [Locator](./locator.md) | [MDIClient](./mdiclient.md) | [Menu](./menu.md) | [MenuItem](./menuitem.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) | [RichEdit](./richedit.md) | [Root](./root.md) | [Scroll](./scroll.md) | [Separator](./separator.md) | [SM](./sm.md) | [Spinner](./spinner.md) | [Splitter](./splitter.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) | [TabButton](./tabbutton.md) | [TabControl](./tabcontrol.md) | [ToolBar](./toolbar.md) | [ToolButton](./toolbutton.md) | [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |  |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) |
| [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) |
| [Combo](./combo.md) | [ComboEx](./comboex.md) | [CoolBand](./coolband.md) |
| [CoolBar](./coolbar.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) |
| [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) |
| [HTMLRenderer](./htmlrenderer.md) | [Label](./label.md) | [List](./list.md) |
| [ListView](./listview.md) | [Locator](./locator.md) | [MDIClient](./mdiclient.md) |
| [Menu](./menu.md) | [MenuItem](./menuitem.md) | [ProgressBar](./progressbar.md) |
| [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) | [RichEdit](./richedit.md) |
| [Root](./root.md) | [Scroll](./scroll.md) | [Separator](./separator.md) |
| [SM](./sm.md) | [Spinner](./spinner.md) | [Splitter](./splitter.md) |
| [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) |
| [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) |
| [TabButton](./tabbutton.md) | [TabControl](./tabcontrol.md) | [ToolBar](./toolbar.md) |
| [ToolButton](./toolbutton.md) | [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) |
| [TreeView](./treeview.md) | [UpDown](./updown.md) |  |


Description


With the exception of [Menu](./menu.md), [MenuItem](./menuitem.md) and [Separator](./separator.md) objects, Posn is a 2-element numeric vector specifying the y-position and x-position respectively of the top-left corner of the object relative to its parent. For a [Form](./form.md), Posn specifies its position on the screen. The units are defined by the [Coord](coord.md) property.


When specifying Posn for `⎕WC`, you can allow the y-position or x-position to assume a default value by giving the corresponding element a value of `⍬`.


Using `⎕WS`, if you want to set the y-position, but not the x-position, or vice-versa, you should specify `⍬` for the item you don't want to change.


For [Menu](./menu.md), [MenuItem](./menuitem.md) and [Separator](./separator.md) objects, Posn is a single integer that specifies the position at which the object is to be inserted in its parent. For example, to add a new [MenuItem](./menuitem.md) between the third and fourth items in an existing [Menu](./menu.md), you would specify its Posn as 4. For these objects, the value of Posn returned by `⎕WG` is the current index of the object within its parent.



