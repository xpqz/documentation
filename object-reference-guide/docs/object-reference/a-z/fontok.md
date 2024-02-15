




<h1 class="heading"><span class="name">FontOK</span></h1>

Applies To

| Applies To: | [ActiveXControl](./activexcontrol.md) [Button](./button.md) [ButtonEdit](./buttonedit.md) [Calendar](./calendar.md) [Combo](./combo.md) [ComboEx](./comboex.md) [DateTimePicker](./datetimepicker.md) [Edit](./edit.md) [Font](./font.md) [Form](./form.md) [Grid](./grid.md) [Group](./group.md) [Label](./label.md) [List](./list.md) [ListView](./listview.md) [PropertyPage](./propertypage.md) [PropertySheet](./propertysheet.md) [RichEdit](./richedit.md) [Root](./root.md) [Spinner](./spinner.md) [Static](./static.md) [StatusBar](./statusbar.md) [SubForm](./subform.md) [TabBtn](./tabbtn.md) [Text](./text.md) [TipField](./tipfield.md) [TreeView](./treeview.md) | [ActiveXControl](./activexcontrol.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Calendar](./calendar.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) | [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Font](./font.md) | [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) | [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) | [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) | [RichEdit](./richedit.md) | [Root](./root.md) | [Spinner](./spinner.md) | [Static](./static.md) | [StatusBar](./statusbar.md) | [SubForm](./subform.md) | [TabBtn](./tabbtn.md) | [Text](./text.md) | [TipField](./tipfield.md) | [TreeView](./treeview.md) |
| --- | --- | ---  |
| [ActiveXControl](./activexcontrol.md) | [Button](./button.md) | [ButtonEdit](./buttonedit.md) |
| [Calendar](./calendar.md) | [Combo](./combo.md) | [ComboEx](./comboex.md) |
| [DateTimePicker](./datetimepicker.md) | [Edit](./edit.md) | [Font](./font.md) |
| [Form](./form.md) | [Grid](./grid.md) | [Group](./group.md) |
| [Label](./label.md) | [List](./list.md) | [ListView](./listview.md) |
| [PropertyPage](./propertypage.md) | [PropertySheet](./propertysheet.md) | [RichEdit](./richedit.md) |
| [Root](./root.md) | [Spinner](./spinner.md) | [Static](./static.md) |
| [StatusBar](./statusbar.md) | [SubForm](./subform.md) | [TabBtn](./tabbtn.md) |
| [Text](./text.md) | [TipField](./tipfield.md) | [TreeView](./treeview.md) |


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



