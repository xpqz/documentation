




<h1 class="heading"><span class="name">Translate</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Animation](./animation.md) [Bitmap](./bitmap.md) [BrowseBox](./browsebox.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Clipboard](./clipboard.md) [ColorButton](./colorbutton.md) [Combo](./combo.md) [ComboEx](./comboex.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [HTMLRenderer](./htmlrenderer.md) [ImageList](./imagelist.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [MDIClient](./mdiclient.md) [Menu](./menu.md) [MenuBar](./menubar.md) [MenuItem](./menuitem.md) [Metafile](./metafile.md) [OCXClass](./ocxclass.md) [Printer](./printer.md) [ProgressBar](./progressbar.md) [PropertyPage](./propertypage.md) [PropertySheet](./propertysheet.md) [RichEdit](./richedit.md) [Root](./root.md) [Scroll](./scroll.md) [Separator](./separator.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [StatusField](./statusfield.md) [SubForm](./subform.md) [SysTrayItem](./systrayitem.md) [TabBar](./tabbar.md) [TabBtn](./tabbtn.md) [Text](./text.md) [TipField](./tipfield.md) [ToolBar](./toolbar.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) [UpDown](./updown.md) | [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Bitmap](./bitmap.md) | [BrowseBox](./browsebox.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Clipboard](./clipboard.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [HTMLRenderer](./htmlrenderer.md) | [ImageList](./imagelist.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [MDIClient](./mdiclient.md) | [Menu](./menu.md) | [MenuBar](./menubar.md) | [MenuItem](./menuitem.md) | [Metafile](./metafile.md) | [OCXClass](./ocxclass.md) | [Printer](./printer.md) | [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) | [RichEdit](./richedit.md) | [Root](./root.md) | [Scroll](./scroll.md) | [Separator](./separator.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) | [SubForm](./subform.md) | [SysTrayItem](./systrayitem.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) | [Text](./text.md) | [TipField](./tipfield.md) | [ToolBar](./toolbar.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Animation](./animation.md) | [Bitmap](./bitmap.md) |
| [BrowseBox](./browsebox.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) |
| [Clipboard](./clipboard.md) | [ColorButton](./colorbutton.md) | [Combo](./combo.md) |
| [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) |
| [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) |
| [HTMLRenderer](./htmlrenderer.md) | [ImageList](./imagelist.md) | [Label](./label.md) |
| [List](./list.md) | [ListView](./listview.md) | [MDIClient](./mdiclient.md) |
| [Menu](./menu.md) | [MenuBar](./menubar.md) | [MenuItem](./menuitem.md) |
| [Metafile](./metafile.md) | [OCXClass](./ocxclass.md) | [Printer](./printer.md) |
| [ProgressBar](./progressbar.md) | [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) |
| [RichEdit](./richedit.md) | [Root](./root.md) | [Scroll](./scroll.md) |
| [Separator](./separator.md) | [Spinner](./spinner.md) | [Static](./static.md) |
| [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) | [SubForm](./subform.md) |
| [SysTrayItem](./systrayitem.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) |
| [Text](./text.md) | [TipField](./tipfield.md) | [ToolBar](./toolbar.md) |
| [TrackBar](./trackbar.md) | [TreeView](./treeview.md) | [UpDown](./updown.md) |


Description


This property specifies whether or not character data is to be translated.



Translate applies to the Classic Edition only. In the Unicode Edition,
			its value is ignored.


Translate is a character vector whose values may be `'Inherit'`,
`'Translate'`, `'ANSI'` or `'None'`.


A value of `'Translate'` means that all
character property values and event parameters are translated to and from `⎕AV` using the current output translation table (WIN.DOT).


`'None'` means that character data is
passed between APL and the object with no translation.


If you set the value of the Translate property to `'ANSI'`,
APL does not attempt to resolve characters as they are typed by the user via the
Input Translate Table. Using Translate `'ANSI'` in combination with the appropriate value of CharSet and the corresponding National Language keyboard will permit users to enter
strings in non-western languages.


`'Inherit'` means that the object
inherits its translation from its parent.


The default value for the Root and Printer objects is `'Translate'`,
and for most other objects it is `'Inherit'`.


