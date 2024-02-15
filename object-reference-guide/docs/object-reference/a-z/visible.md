




<h1 class="heading"><span class="name">Visible</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Animation](./animation.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [Circle](./circle.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [CoolBand](./coolband.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Ellipse](./ellipse.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [HTMLRenderer](./htmlrenderer.md) [Image](./image.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [Marker](./marker.md) [MenuBar](./menubar.md) [Poly](./poly.md) [ProgressBar](./progressbar.md) [PropertySheet](./propertysheet.md) [Rect](./rect.md) [RichEdit](./richedit.md) [Scroll](./scroll.md) [SM](./sm.md) [Spinner](./spinner.md) [Splitter](./splitter.md) [Static](./static.md) [StatusBar](./statusbar.md) [StatusField](./statusfield.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [TabBtn](./tabbtn.md) [TabControl](./tabcontrol.md) [Text](./text.md) [ToolBar](./toolbar.md) [ToolButton](./toolbutton.md) [ToolControl](./toolcontrol.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [Circle](./circle.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [CoolBand](./coolband.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Ellipse](./ellipse.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [HTMLRenderer](./htmlrenderer.md) | [Image](./image.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [Marker](./marker.md) | [MenuBar](./menubar.md) | [Poly](./poly.md) | [ProgressBar](./progressbar.md) | [PropertySheet](./propertysheet.md) | [Rect](./rect.md) | [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) | [Splitter](./splitter.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) | [TabControl](./tabcontrol.md) | [Text](./text.md) | [ToolBar](./toolbar.md) | [ToolButton](./toolbutton.md) | [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Button](./button.md) |
| [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [Circle](./circle.md) |
| [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) |
| [CoolBand](./coolband.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) |
| [Ellipse](./ellipse.md) | [Form](./form.md) | [Grid](./grid.md) |
| [Group](./group.md) | [HTMLRenderer](./htmlrenderer.md) | [Image](./image.md) |
| [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) |
| [Marker](./marker.md) | [MenuBar](./menubar.md) | [Poly](./poly.md) |
| [ProgressBar](./progressbar.md) | [PropertySheet](./propertysheet.md) | [Rect](./rect.md) |
| [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [SM](./sm.md) |
| [Spinner](./spinner.md) | [Splitter](./splitter.md) | [Static](./static.md) |
| [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) | [SubForm](./subform.md) |
| [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) | [TabControl](./tabcontrol.md) |
| [Text](./text.md) | [ToolBar](./toolbar.md) | [ToolButton](./toolbutton.md) |
| [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) |
| [UpDown](./updown.md) |  |  |


Description


This property specifies whether or not an object is currently visible. It is a single number with the value 0 (object is invisible) or 1 (object is visible). The default is 1. Setting Visible on and off is a way to pop a dialog box up and down as required.


Note that an invisible object is not necessarily inactive, and is capable of generating events. For example, a [Button](./button.md) with a [Cancel](cancel.md) property of 1 will generate a [Select](./select.md) (30) event (if enabled) whether or not it is visible. An invisible object will also respond to methods and  events sent to it by `⎕NQ`.



