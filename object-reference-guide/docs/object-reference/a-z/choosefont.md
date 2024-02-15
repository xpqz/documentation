



<h1 class="heading"><span class="name">ChooseFont</span></h1>

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


This method is used to display the standard Windows font selection dialog box.


The argument to ChooseFont is `⍬` or a 1 or 2-element array as follows:

| `[1]` | Printer name | character scalar or vector. |
| --- | --- | ---  |
| `[2]` | Modify flag | 0 or 1. |


If the argument is `⍬` or the first element of the argument is `''`, the user is offered a list of fonts suitable for use on the screen. If not, the user is offered a choice of fonts suitable for the specified [Printer](./printer.md) object. If you omit the 2nd element, the modify flag defaults to 0.


The dialog box is initialised with the properties of the [Font](./font.md) object specified in the first element of the event message.


When the user presses the "OK" button, the "Cancel" button or closes the dialog box, ChooseFont terminates. Its result is either 0 (user pressed "Cancel") or a 2-element vector. In the latter case, the first element is an 8-element array that describes the selected font as described below, and the second element is a 3-element RGB colour vector.

| `[1]` | Face name of selected font (character vector) |
| --- | ---  |
| `[2]` | Character height in pixels (integer) |
| `[3]` | Fixed width or not (Boolean) |
| `[4]` | Italic or not (Boolean) |
| `[5]` | Underline or not (Boolean) |
| `[6]` | Weight (integer) |
| `[7]` | Angle of rotation (integer) |
| `[8]` | Character set (see [CharSet](./charset.md) ) |


If the modify flag was 1, the [Font](./font.md) object is redefined to match the user's selections and all the objects that reference the [Font](./font.md) are redrawn.


