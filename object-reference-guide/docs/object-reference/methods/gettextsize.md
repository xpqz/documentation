




<h1 class="heading"><span class="name">GetTextSize</span></h1>

Applies To

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) [Animation](../a-z/animation.md) [Bitmap](../a-z/bitmap.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [ColorButton](../a-z/colorbutton.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [CoolBar](../a-z/coolbar.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Form](../a-z/form.md) [Grid](../a-z/grid.md) [Group](../a-z/group.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [MDIClient](../a-z/mdiclient.md) [Printer](../a-z/printer.md) [ProgressBar](../a-z/progressbar.md) [PropertyPage](../a-z/propertypage.md) [RichEdit](../a-z/richedit.md) [Root](../a-z/root.md) [Scroll](../a-z/scroll.md) [SM](../a-z/sm.md) [Spinner](../a-z/spinner.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [SubForm](../a-z/subform.md) [TabBar](../a-z/tabbar.md) [TabControl](../a-z/tabcontrol.md) [ToolBar](../a-z/toolbar.md) [ToolControl](../a-z/toolcontrol.md) [TrackBar](../a-z/trackbar.md) [TreeView](../a-z/treeview.md) [UpDown](../a-z/updown.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Bitmap](../a-z/bitmap.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [CoolBar](../a-z/coolbar.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [MDIClient](../a-z/mdiclient.md) | [Printer](../a-z/printer.md) | [ProgressBar](../a-z/progressbar.md) | [PropertyPage](../a-z/propertypage.md) | [RichEdit](../a-z/richedit.md) | [Root](../a-z/root.md) | [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [TabControl](../a-z/tabcontrol.md) | [ToolBar](../a-z/toolbar.md) | [ToolControl](../a-z/toolcontrol.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) | [UpDown](../a-z/updown.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) | [Animation](../a-z/animation.md) | [Bitmap](../a-z/bitmap.md) |
| [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) |
| [ColorButton](../a-z/colorbutton.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) |
| [CoolBar](../a-z/coolbar.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) |
| [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) |
| [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) |
| [MDIClient](../a-z/mdiclient.md) | [Printer](../a-z/printer.md) | [ProgressBar](../a-z/progressbar.md) |
| [PropertyPage](../a-z/propertypage.md) | [RichEdit](../a-z/richedit.md) | [Root](../a-z/root.md) |
| [Scroll](../a-z/scroll.md) | [SM](../a-z/sm.md) | [Spinner](../a-z/spinner.md) |
| [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) |
| [TabBar](../a-z/tabbar.md) | [TabControl](../a-z/tabcontrol.md) | [ToolBar](../a-z/toolbar.md) |
| [ToolControl](../a-z/toolcontrol.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) |
| [UpDown](../a-z/updown.md) |  |  |


Description


The GetTextSize method obtains the size of the bounding rectangle of a text item in a given font. The result is given in the co-ordinate system of the object in question. This method is useful for positioning Text objects.



GetTextSize duplicates the functionality of the TextSize property. It is recommended that you use GetTextSize instead of TextSize which may be removed in a future release of Dyalog APL.



The argument to GetTextSize is a 1 or 2-element array as follows:

| `[1]` | Text item | character array |
| --- | --- | ---  |
| `[2]` | Font name | character vector |



When you invoke GetTextSize you give the text item in whose size you are interested and, optionally, the name of a Font object. The text item may be a simple scalar, a vector or a matrix. If the Font is omitted, the result is given using the current font for the object in question.

#### Examples
```apl
      'F'⎕WC'Form'
      F.GetTextSize'Hello World'
3.385416667 10.7421875

      'FNT1' ⎕WC 'Font' 'Arial' 72
      F.GetTextSize'Hello World'  '#.FNT1'
18.75 65.4296875

      F.Coord←'Pixel'
      F.FontObj←'FNT1'
      F.GetTextSize'Hello World'
16 77
```


