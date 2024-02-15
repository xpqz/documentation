




<h1 class="heading"><span class="name">GetTextSize</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Animation](./animation.md) [Bitmap](./bitmap.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [CoolBar](./coolbar.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [MDIClient](./mdiclient.md) [Printer](./printer.md) [ProgressBar](./progressbar.md) [PropertyPage](./propertypage.md) [RichEdit](./richedit.md) [Root](./root.md) [Scroll](./scroll.md) [SM](./sm.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [TabControl](./tabcontrol.md) [ToolBar](./toolbar.md) [ToolControl](./toolcontrol.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Bitmap](./bitmap.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [CoolBar](./coolbar.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [MDIClient](./mdiclient.md) | [Printer](./printer.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [RichEdit](./richedit.md) | [Root](./root.md) | [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabControl](./tabcontrol.md) | [ToolBar](./toolbar.md) | [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |  |  |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Bitmap](./bitmap.md) |
| [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) |
| [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) |
| [CoolBar](./coolbar.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) |
| [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) |
| [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) |
| [MDIClient](./mdiclient.md) | [Printer](./printer.md) | [ProgressBar](./progressbar.md) |
| [PropertyPage](./propertypage.md) | [RichEdit](./richedit.md) | [Root](./root.md) |
| [Scroll](./scroll.md) | [SM](./sm.md) | [Spinner](./spinner.md) |
| [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) |
| [TabBar](./tabbar.md) | [TabControl](./tabcontrol.md) | [ToolBar](./toolbar.md) |
| [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) |
| [UpDown](./updown.md) |  |  |


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


