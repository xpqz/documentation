




<h1 class="heading"><span class="name">Sizeable</span></h1>

Applies To

| Applies To: | [Animation](./animation.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [HTMLRenderer](./htmlrenderer.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [Locator](./locator.md) [ProgressBar](./progressbar.md) [RichEdit](./richedit.md) [Scroll](./scroll.md) [SM](./sm.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [StatusField](./statusfield.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [ToolBar](./toolbar.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [HTMLRenderer](./htmlrenderer.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [Locator](./locator.md) | [ProgressBar](./progressbar.md) | [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [ToolBar](./toolbar.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |  |  |
| --- | --- | ---  |
| [Animation](./animation.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) |
| [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) |
| [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) |
| [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) |
| [HTMLRenderer](./htmlrenderer.md) | [Label](./label.md) | [List](./list.md) |
| [ListView](./listview.md) | [Locator](./locator.md) | [ProgressBar](./progressbar.md) |
| [RichEdit](./richedit.md) | [Scroll](./scroll.md) | [SM](./sm.md) |
| [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) |
| [StatusField](./statusfield.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) |
| [ToolBar](./toolbar.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) |
| [UpDown](./updown.md) |  |  |


Description


This property determines whether or not an object can be directly resized by the user once it has been created by `⎕WC`.



It is a single number with the value 0 (the object cannot be resized by the user) or 1 (the object may be resized by the user). The default is 1.


For a [Form](./form.md) , [HTMLRenderer](./htmlrenderer.md) or [SubForm](./subform.md), the Sizeable property may only be set by `⎕WC` and cannot subsequently be altered using `⎕WS`. An attempt to do so generates a `NONCE ERROR`. For a [Form](./form.md) or [HTMLRenderer](./htmlrenderer.md), the default value is 1 and the object occupies a standard resizeable window with a border. Note that the value of Sizeable is independent of the values of the [MaxButton](maxbutton.md) and [MinButton](minbutton.md) properties, so that a [Form](./form.md) or [HTMLRenderer](./htmlrenderer.md) with [MaxButton](maxbutton.md) 1 can be maximised even though its Sizeable property is 0.


For other objects, the default value of the Sizeable property is 0. However, setting it to 1 (which may be done dynamically using `⎕WS`) allows the user to resize it with the mouse.


In all these cases, when the user resizes an object, the object will generate a [Configure](./configure.md) (31) event.


Sizeable also applies to the [Locator](./locator.md) object. In this case, a value of 1 implies "rubberbanding" and a value of 0 means "no rubberbanding". See [Locator](./locator.md) object for further details.


