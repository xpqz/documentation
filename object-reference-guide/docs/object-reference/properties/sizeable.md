




<h1 class="heading"><span class="name">Sizeable</span></h1>

Applies To

| Applies To: | [Animation](../a-z/animation.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [ColorButton](../a-z/colorbutton.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Form](../a-z/form.md) [Grid](../a-z/grid.md) [Group](../a-z/group.md) [HTMLRenderer](../a-z/htmlrenderer.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [Locator](../a-z/locator.md) [ProgressBar](../a-z/progressbar.md) [RichEdit](../a-z/richedit.md) [Scroll](../a-z/scroll.md) [SM](../a-z/sm.md) [Spinner](../a-z/spinner.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [StatusField](../a-z/statusfield.md) [SubForm](../a-z/subform.md) [TabBar](../a-z/tabbar.md) [ToolBar](../a-z/toolbar.md) [TrackBar](../a-z/trackbar.md) [TreeView](../a-z/treeview.md) [UpDown](../a-z/updown.md) | [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [HTMLRenderer](../a-z/htmlrenderer.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [Locator](../a-z/locator.md) | [ProgressBar](../a-z/progressbar.md) | [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [StatusField](../a-z/statusfield.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [ToolBar](../a-z/toolbar.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |  |  |
| --- | --- | ---  |
| [Animation](../a-z/animation.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) |
| [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) |
| [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) |
| [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) |
| [HTMLRenderer](../a-z/htmlrenderer.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) |
| [ListView](../a-z/listview.md) | [Locator](../a-z/locator.md) | [ProgressBar](../a-z/progressbar.md) |
| [RichEdit](../a-z/richedit.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) |
| [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) |
| [StatusField](../a-z/statusfield.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) |
| [ToolBar](../a-z/toolbar.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) |
| [UpDown](../a-z/updown.md) |  |  |


Description


This property determines whether or not an object can be directly resized by the user once it has been created by `⎕WC`.



It is a single number with the value 0 (the object cannot be resized by the user) or 1 (the object may be resized by the user). The default is 1.


For a [Form](../a-z/form.md) , [HTMLRenderer](../a-z/htmlrenderer.md) or [SubForm](../a-z/subform.md), the Sizeable property may only be set by `⎕WC` and cannot subsequently be altered using `⎕WS`. An attempt to do so generates a `NONCE ERROR`. For a [Form](../a-z/form.md) or [HTMLRenderer](../a-z/htmlrenderer.md), the default value is 1 and the object occupies a standard resizeable window with a border. Note that the value of Sizeable is independent of the values of the [MaxButton](../a-z/maxbutton.md) and [MinButton](../a-z/minbutton.md) properties, so that a [Form](../a-z/form.md) or [HTMLRenderer](../a-z/htmlrenderer.md) with [MaxButton](../a-z/maxbutton.md) 1 can be maximised even though its Sizeable property is 0.


For other objects, the default value of the Sizeable property is 0. However, setting it to 1 (which may be done dynamically using `⎕WS`) allows the user to resize it with the mouse.


In all these cases, when the user resizes an object, the object will generate a [Configure](../a-z/configure.md) (31) event.


Sizeable also applies to the [Locator](../a-z/locator.md) object. In this case, a value of 1 implies "rubberbanding" and a value of 0 means "no rubberbanding". See [Locator](../a-z/locator.md) object for further details.


