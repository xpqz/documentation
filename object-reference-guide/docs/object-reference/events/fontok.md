




<h1 class="heading"><span class="name">FontOK</span></h1>

Applies To

| Applies To: | [ActiveXControl](../a-z/activexcontrol.md) [Button](../a-z/button.md) [ButtonEdit](../a-z/buttonedit.md) [Calendar](../a-z/calendar.md) [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) [DateTimePicker](../a-z/datetimepicker.md) [Edit](../a-z/edit.md) [Font](../a-z/font.md) [Form](../a-z/form.md) [Grid](../a-z/grid.md) [Group](../a-z/group.md) [Label](../a-z/label.md) [List](../a-z/list.md) [ListView](../a-z/listview.md) [PropertyPage](../a-z/propertypage.md) [PropertySheet](../a-z/propertysheet.md) [RichEdit](../a-z/richedit.md) [Root](../a-z/root.md) [Spinner](../a-z/spinner.md) [Static](../a-z/static.md) [StatusBar](../a-z/statusbar.md) [SubForm](../a-z/subform.md) [TabBtn](../a-z/tabbtn.md) [Text](../a-z/text.md) [TipField](../a-z/tipfield.md) [TreeView](../a-z/treeview.md) | [ActiveXControl](../a-z/activexcontrol.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Calendar](../a-z/calendar.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) | [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Font](../a-z/font.md) | [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) | [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) | [PropertyPage](../a-z/propertypage.md) | [PropertySheet](../a-z/propertysheet.md) | [RichEdit](../a-z/richedit.md) | [Root](../a-z/root.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) | [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBtn](../a-z/tabbtn.md) | [Text](../a-z/text.md) | [TipField](../a-z/tipfield.md) | [TreeView](../a-z/treeview.md) |
| --- | --- | ---  |
| [ActiveXControl](../a-z/activexcontrol.md) | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) |
| [Calendar](../a-z/calendar.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) |
| [DateTimePicker](../a-z/datetimepicker.md) | [Edit](../a-z/edit.md) | [Font](../a-z/font.md) |
| [Form](../a-z/form.md) | [Grid](../a-z/grid.md) | [Group](../a-z/group.md) |
| [Label](../a-z/label.md) | [List](../a-z/list.md) | [ListView](../a-z/listview.md) |
| [PropertyPage](../a-z/propertypage.md) | [PropertySheet](../a-z/propertysheet.md) | [RichEdit](../a-z/richedit.md) |
| [Root](../a-z/root.md) | [Spinner](../a-z/spinner.md) | [Static](../a-z/static.md) |
| [StatusBar](../a-z/statusbar.md) | [SubForm](../a-z/subform.md) | [TabBtn](../a-z/tabbtn.md) |
| [Text](../a-z/text.md) | [TipField](../a-z/tipfield.md) | [TreeView](../a-z/treeview.md) |


Description


If enabled, this event is reported when the user has pressed the *OK* button in the font selection dialog box that is displayed by the ChooseFont method.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 4-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'FontOK'` or 241 |
| `[3]` | Font | nested vector |
| `[4]` | Colour | RGB triplet |


The font specification in the 3rd element of the event message is a 7-element nested vector that describes the chosen font. See Font Object for further details.


The colour specification in the 4th element of the event message is a 3-element integer vector of RGB values for the colour chosen by the user.



