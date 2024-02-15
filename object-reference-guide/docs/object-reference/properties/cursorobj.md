




<h1 class="heading"><span class="name">CursorObj</span></h1>

Applies To

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [Circle](../a-z/circle.md) [ColorButton](../a-z/colorbutton.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [CoolBar](../a-z/coolbar.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Ellipse](../a-z/ellipse.md) [Form](../a-z/form.md) [Grid](../a-z/grid.md) [Group](../a-z/group.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [Locator](../a-z/locator.md) [MDIClient](../a-z/mdiclient.md) [Poly](../a-z/poly.md) [ProgressBar](../a-z/progressbar.md) [Rect](../a-z/rect.md) [RichEdit](../a-z/richedit.md) [Root](../a-z/root.md) [Scroll](../a-z/scroll.md) [SM](../a-z/sm.md) [Spinner](../a-z/spinner.md) [Splitter](../a-z/splitter.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [SubForm](../a-z/subform.md) [TabBar](../a-z/tabbar.md) [Text](../a-z/text.md) [ToolBar](../a-z/toolbar.md) [TrackBar](../a-z/trackbar.md) [TreeView](../a-z/treeview.md) [UpDown](../a-z/updown.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [Circle](../a-z/circle.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [CoolBar](../a-z/coolbar.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Ellipse](../a-z/ellipse.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [Locator](../a-z/locator.md) | [MDIClient](../a-z/mdiclient.md) | [Poly](../a-z/poly.md) | [ProgressBar](../a-z/progressbar.md) | [Rect](../a-z/rect.md) | [RichEdit](../a-z/richedit.md) | [Root](../a-z/root.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) | [Splitter](../a-z/splitter.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [Text](../a-z/text.md) | [ToolBar](../a-z/toolbar.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |  |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) |
| [Calendar](../a-z/calendar.md) | [Circle](../a-z/circle.md) | [ColorButton](../a-z/colorbutton.md) |
| [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [CoolBar](../a-z/coolbar.md) |
| [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Ellipse](../a-z/ellipse.md) |
| [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) |
| [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) |
| [Locator](../a-z/locator.md) | [MDIClient](../a-z/mdiclient.md) | [Poly](../a-z/poly.md) |
| [ProgressBar](../a-z/progressbar.md) | [Rect](../a-z/rect.md) | [RichEdit](../a-z/richedit.md) |
| [Root](../a-z/root.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) |
| [Spinner](../a-z/spinner.md) | [Splitter](../a-z/splitter.md) | [Static](../a-z/static.md) |
| [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) |
| [Text](../a-z/text.md) | [ToolBar](../a-z/toolbar.md) | [TrackBar](../a-z/trackbar.md) |
| [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |  |


Description


This property is used to associate a particular cursor with an object.




Its
value is either a simple scalar number which specifies a standard Windows
cursor, or the name of, or ref to, a [Cursor](../a-z/cursor.md) object. The standard Windows cursors are :

| 0 | arrow (Windows default) |
| --- | ---  |
| 1 | hourglass |
| 2 | crosshair |
| 3 | I-Beam |
| 4 | crossing vertical/horizontal double-headed arrows |
| 5 | diagonal double-headed arrows (left-to-right) |
| 6 | vertical double-headed arrows |
| 7 | diagonal double-headed arrows (right-to-left) |
| 8 | horizontal double-headed arrows |
| 9 | upward pointing arrow |
| 10 | box |
| 11 | crossing vertical/horizontal double-headed arrows |
| 12 | no-entry sign |
| 13 | arrow with hourglass |
| 14 | pointing hand |



If CursorObj is set to anything other than an empty vector (which is the
default) it defines the appearance of the cursor when the mouse pointer is moved
into the object. If CursorObj is an empty vector, the shape of the cursor
remains unchanged when the mouse pointer enters the object. In effect, the
cursor is "inherited" from its parent. Exceptions to this rule are
certain objects which have special cursors by default.



If the value of CursorObj for the [Root](../a-z/root.md) object
is set to anything other than an empty vector, it applies to all[ Form](../a-z/form.md)s
and their children, irrespective of their own CursorObj values. Therefore, if
you want to indicate that your application is "working" and is not
responsive to input, you can simply do:
```apl
      '.' ⎕WS 'CursorObj' 1 ⍝ Hourglass cursor
```


Then to reset the application you do:
```apl
      '.' ⎕WS 'CursorObj' ''
```



