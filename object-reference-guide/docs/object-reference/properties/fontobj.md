




<h1 class="heading"><span class="name">FontObj</span></h1>

Applies To

| Applies To: | [ActiveXContainer](../a-z/activexcontainer.md) [ActiveXControl](../a-z/activexcontrol.md) [Bitmap](../a-z/bitmap.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Form](../a-z/form.md) [Grid](../a-z/grid.md) [Group](../a-z/group.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [Menu](../a-z/menu.md) [MenuBar](../a-z/menubar.md) [MenuItem](../a-z/menuitem.md) [Printer](../a-z/printer.md) [PropertyPage](../a-z/propertypage.md) [PropertySheet](../a-z/propertysheet.md) [RichEdit](../a-z/richedit.md) [Root](../a-z/root.md) [Spinner](../a-z/spinner.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [StatusField](../a-z/statusfield.md) [SubForm](../a-z/subform.md) [TabBar](../a-z/tabbar.md) [TabBtn](../a-z/tabbtn.md) [TabControl](../a-z/tabcontrol.md) [Text](../a-z/text.md) [TipField](../a-z/tipfield.md) [ToolBar](../a-z/toolbar.md) [ToolControl](../a-z/toolcontrol.md) [TrackBar](../a-z/trackbar.md) [TreeView](../a-z/treeview.md) | [ActiveXContainer](../a-z/activexcontainer.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Bitmap](../a-z/bitmap.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [Menu](../a-z/menu.md) | [MenuBar](../a-z/menubar.md) | [MenuItem](../a-z/menuitem.md) | [Printer](../a-z/printer.md) | [PropertyPage](../a-z/propertypage.md) | [PropertySheet](../a-z/propertysheet.md) | [RichEdit](../a-z/richedit.md) | [Root](../a-z/root.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [StatusField](../a-z/statusfield.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) | [TabBtn](../a-z/tabbtn.md) | [TabControl](../a-z/tabcontrol.md) | [Text](../a-z/text.md) | [TipField](../a-z/tipfield.md) | [ToolBar](../a-z/toolbar.md) | [ToolControl](../a-z/toolcontrol.md) | [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) |  |
| --- | --- | ---  |
| [ActiveXContainer](../a-z/activexcontainer.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Bitmap](../a-z/bitmap.md) |
| [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) |
| [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) |
| [Edit](../a-z/edit.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) |
| [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) |
| [ListView](../a-z/listview.md) | [Menu](../a-z/menu.md) | [MenuBar](../a-z/menubar.md) |
| [MenuItem](../a-z/menuitem.md) | [Printer](../a-z/printer.md) | [PropertyPage](../a-z/propertypage.md) |
| [PropertySheet](../a-z/propertysheet.md) | [RichEdit](../a-z/richedit.md) | [Root](../a-z/root.md) |
| [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) |
| [StatusField](../a-z/statusfield.md) | [SubForm](../a-z/subform.md) | [TabBar](../a-z/tabbar.md) |
| [TabBtn](../a-z/tabbtn.md) | [TabControl](../a-z/tabcontrol.md) | [Text](../a-z/text.md) |
| [TipField](../a-z/tipfield.md) | [ToolBar](../a-z/toolbar.md) | [ToolControl](../a-z/toolcontrol.md) |
| [TrackBar](../a-z/trackbar.md) | [TreeView](../a-z/treeview.md) |  |


Description


The FontObj property associates a font with an object. It specifies either the name of or a ref to a [Font](../a-z/font.md) object


If unspecified, the default value for FontObj is an empty character vector. For most objects, this setting implies that the font used in the object is inherited from its parent object. However, [CoolBar](../a-z/coolbar.md), [Menu](../a-z/menu.md), [MenuBar](../a-z/menubar.md), [StatusBar](../a-z/statusbar.md), [TipField](../a-z/tipfield.md), [ToolBar](../a-z/toolbar.md), and [ToolControl](../a-z/toolcontrol.md) objects do not inherit their font.


Note that the default value of FontObj for [Root](../a-z/root.md) is also an empty character vector and that this implies the Windows default GUI font, which is a Windows user preference setting.


Note however that it is not currently possible to specify the font for [Menu](../a-z/menu.md) and [MenuItem](../a-z/menuitem.md) objects which are the direct descendants of a [MenuBar](../a-z/menubar.md). Nor is it possible to specify the font used for the [Caption](../a-z/caption.md) in a [Form](../a-z/form.md).



