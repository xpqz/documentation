




<h1 class="heading"><span class="name">FontObj</span></h1>

Applies To

| Applies To: | [ActiveXContainer](./activexcontainer.md) [ActiveXControl](./activexcontrol.md) [Bitmap](./bitmap.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [Combo](./combo.md) [ComboEx](./comboex.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [Menu](./menu.md) [MenuBar](./menubar.md) [MenuItem](./menuitem.md) [Printer](./printer.md) [PropertyPage](./propertypage.md) [PropertySheet](./propertysheet.md) [RichEdit](./richedit.md) [Root](./root.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [StatusField](./statusfield.md) [SubForm](./subform.md) [TabBar](./tabbar.md) [TabBtn](./tabbtn.md) [TabControl](./tabcontrol.md) [Text](./text.md) [TipField](./tipfield.md) [ToolBar](./toolbar.md) [ToolControl](./toolcontrol.md) [TrackBar](./trackbar.md) [TreeView](./treeview.md) | [ActiveXContainer](./activexcontainer.md) | [ActiveXControl](./activexcontrol.md) | [Bitmap](./bitmap.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [Menu](./menu.md) | [MenuBar](./menubar.md) | [MenuItem](./menuitem.md) | [Printer](./printer.md) | [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) | [RichEdit](./richedit.md) | [Root](./root.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [StatusField](./statusfield.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) | [TabControl](./tabcontrol.md) | [Text](./text.md) | [TipField](./tipfield.md) | [ToolBar](./toolbar.md) | [ToolControl](./toolcontrol.md) | [TrackBar](./trackbar.md) | [TreeView](./treeview.md) |  |
| --- | --- | ---  |
| [ActiveXContainer](./activexcontainer.md) | [ActiveXControl](./activexcontrol.md) | [Bitmap](./bitmap.md) |
| [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) |
| [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) |
| [Edit](./edit.md) | [Form](./form.md) | [Grid](./grid.md) |
| [Group](./group.md) | [Label](./label.md) | [List](./list.md) |
| [ListView](./listview.md) | [Menu](./menu.md) | [MenuBar](./menubar.md) |
| [MenuItem](./menuitem.md) | [Printer](./printer.md) | [PropertyPage](./propertypage.md) |
| [PropertySheet](./propertysheet.md) | [RichEdit](./richedit.md) | [Root](./root.md) |
| [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) |
| [StatusField](./statusfield.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) |
| [TabBtn](./tabbtn.md) | [TabControl](./tabcontrol.md) | [Text](./text.md) |
| [TipField](./tipfield.md) | [ToolBar](./toolbar.md) | [ToolControl](./toolcontrol.md) |
| [TrackBar](./trackbar.md) | [TreeView](./treeview.md) |  |


Description


The FontObj property associates a font with an object. It specifies either the name of or a ref to a [Font](./font.md) object


If unspecified, the default value for FontObj is an empty character vector. For most objects, this setting implies that the font used in the object is inherited from its parent object. However, [CoolBar](./coolbar.md), [Menu](./menu.md), [MenuBar](./menubar.md), [StatusBar](./statusbar.md), [TipField](./tipfield.md), [ToolBar](./toolbar.md), and [ToolControl](./toolcontrol.md) objects do not inherit their font.


Note that the default value of FontObj for [Root](./root.md) is also an empty character vector and that this implies the Windows default GUI font, which is a Windows user preference setting.


Note however that it is not currently possible to specify the font for [Menu](./menu.md) and [MenuItem](./menuitem.md) objects which are the direct descendants of a [MenuBar](./menubar.md). Nor is it possible to specify the font used for the [Caption](caption.md) in a [Form](./form.md).



