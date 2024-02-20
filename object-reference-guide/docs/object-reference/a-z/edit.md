




<h1 class="heading"><span class="name">Edit</span></h1>

[Parents](../ParentLists/Edit.htm) [Children](../ChildLists/Edit.htm) [Properties](../PropLists/Edit.htm) [Methods](../MethodLists/Edit.htm) [Events](../EventLists/Edit.htm)


Purpose: Allows user to enter or edit data.


**Description**


The value of the [Style](./style.md) property, which may be `'Single'` or `'Multi'`, determines whether the object presents a single-line data entry field or an area for viewing and editing a large block of text.

#### Single-Line Edit



The [FieldType](./fieldtype.md) property (which applies only to a single-line Edit object) is either an empty vector (the default) or specifies the type of the field as reflected by its [Value](./value.md) property. If [FieldType](./fieldtype.md) is empty, the [Value](./value.md) of the field may be a number or a character vector, according to the contents defined by its [Text](./text.md) property (this is always a character vector).


The [Align](./align.md) property, which applies only to single-line Edit objects, specifies the vertical alignment of the text. It may be `'None'` (the default), `'Centre'` or `'Center'`. [Align](./align.md) may only be set when the object is created and may not subsequently be changed.


If [FieldType](./fieldtype.md) is `'Char'` the [Value](./value.md) of the field is forced to be a character vector, even if the contents defined by its [Text](./text.md) property is entirely numeric.


If [FieldType](./fieldtype.md) is `'Numeric'`, `'LongNumeric'`, `'Currency'`, `'Date'`, `'LongDate'`, or `'Time'` the [Value](./value.md) contains a number. For fields of these types, basic validation is provided during user input. The field is revalidated when the user attempts to "leave" it and at this point the object will generate a [BadValue](./badvalue.md) event if its contents are inconsistent with its [FieldType](./fieldtype.md).


Note that when an Edit object is used as the [Input](./input.md) property of a [Grid](grid.md), it is the [Value](./value.md) of the Edit object (and not its [Text](./text.md) property) that is used to update the [Values](./values.md) property (i.e. the contents of) the [Grid](grid.md) when the user moves away from the cell.


The [MaxLength](./maxlength.md) property defines the maximum number of characters that the user may enter into the object.


The [ValidIfEmpty](./validifempty.md) property may be 0 (the default) or 1 and specifies whether or not the Edit field is deemed to be valid if it is empty.


The [Password](./password.md) property specifies the character that is displayed in response to the user typing a character. Normally, [Password](./password.md) is empty (the default) and the object displays the character that was entered. However, if you set [Password](./password.md) to (say) an asterisk (*) this symbol will be displayed instead of the characters the user has entered. Note however that the [Text](./text.md) and [Value](./value.md) properties will reflect what the user typed.


The [HScroll](./hscroll.md) property determines whether or not the data may be scrolled. If [HScroll](./hscroll.md) is 0, the data is not scrollable, and the user cannot enter more characters once the field is full. If [HScroll](./hscroll.md) is `¯1` or `¯2` the field is scrollable, and there is no limit on the number of characters that can be entered. In neither case however is a horizontal scrollbar provided. [HScroll](./hscroll.md) may only be set when the object is created and may not subsequently be changed.

#### Multi-Line Edit


If the [Style](./style.md) is `'Multi'`, [Text](./text.md) may set using a simple character vector, a simple matrix, or a vector of vectors. If  [Text](./text.md) is specified by a matrix or by a vector of vectors, "new-line" characters are automatically added at the end of each line in the Edit control.


The user may insert a "new-line" character in the text by pressing Ctrl-Enter. If [Text](./text.md) was set by a matrix, it is returned as a matrix. Otherwise it is returned as a vector of vectors. "New-line" characters are not returned. If [Text](./text.md) was not specified  by [`⎕WC`](../../Language/System Functions/wc.htm) or  [`⎕WS`](../../Language/System Functions/ws.htm) it is returned  an empty matrix (`1 0⍴''`). However,  if [Text](./text.md) was not specified, but the user types and then empties the field, it is returned as an empty nested array  (`,⊂''`)


The [Justify](./justify.md) property determines whether the text in a multi-line Edit object is `'Left'`, `'Right'`, or `'Centre'` justified. Setting [Justify](./justify.md) to `'Centre'` or `'Right'` also forces word-wrapping and disables horizontal scrolling, whatever the value of [HScroll](./hscroll.md). Note that the keyword `'Centre'` may also be spelled `'Center'`. [Justify](./justify.md) may only be specified when the object is created using `⎕WC`.


If [Justify](./justify.md) is `'Left'`, the [HScroll](./hscroll.md) property determines whether or not text may be scrolled horizontally. If [HScroll](./hscroll.md) is set to `¯2`, each individual line may be any length, but the object does not have a horizontal scrollbar. Sideways scrolling is achieved using the cursor keys, or by typing. If [HScroll](./hscroll.md) is `¯1`, each individual line may be of any length and the object will have a horizontal scrollbar. If [HScroll](./hscroll.md) is `0`, lines are automatically "word-wrapped" at the right edge of the object. This means that the number of lines displayed may be greater than the number of lines implied by the rows of the matrix or the number of vectors supplied. In particular, if you specify a single long vector, it will be broken up into lines for you on the display, but still returned as a single vector by [`⎕WG`](../../Language/System Functions/wg.htm).


The [VScroll](./vscroll.md) property determines whether or not data may be scrolled vertically and whether or not the object has a vertical scrollbar. A value of `0` inhibits scrolling; `¯2` means scrollable, without a scrollbar; `¯1` means scrollable with a scrollbar. [VScroll](./vscroll.md) may only be set when the object is created and may not subsequently be changed.


The setting of [Justify](./justify.md) forces word-wrapping.


The [SelText](./seltext.md) property identifies the portion of the text that is selected. It may be used to pre-select (and highlight) a part of the text, or to report the part of the text selected by the user. [SelText](./seltext.md) is a 2-element integer vector which specifies the start and end of the selected area. Its structure depends upon the nature of the data specified by [Text](./text.md). See the description of [SelText](./seltext.md) for details.


If the user changes any data in the field **and** attempts to change focus to another object, the Edit object will generate a [Change](./change.md) event. You can use this to validate the new data in the field.

#### Note


For full functionality (in particular, for the [Cue](./cue.md) property to apply), the Edit object requires that  [Native Look and Feel ](../../Miscellaneous/Windows XP Look and Feel.htm)
[(see page 1)](../../Miscellaneous/Windows XP Look and Feel.htm#Native_Look_and_Feel)
 is enabled.


