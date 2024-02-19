




<h1 class="heading"><span class="name">Combo</span></h1>

| [Parents](../ParentLists/Combo.htm) | [Children](../ChildLists/Combo.htm) | [Properties](../PropLists/Combo.htm) | [Methods](../MethodLists/Combo.htm) | [Events](../EventLists/Combo.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | This object combines an input area with a list box and allows the user to enter a selection by typing text or by choosing an item from the list. |
| --- | ---  |


**Description**


Three types of Combo box are provided by the [Style](./style.md) property which may be `'Drop'` (the default), `'Simple'` or `'DropEdit'`.



The [Items](./items.md) property specifies the list of items which are displayed in the list box and from which the user can choose.


The [SelItems](./selitems.md) property is a Boolean vector which specifies which (if any) of the items is selected. When the user chooses an item from the list, it is copied to the edit field and a [Select](./select.md) event is generated. At this point you may use [SelItems](./selitems.md) to identify the chosen item. You can also use [SelItems](./selitems.md) to pre-select the contents of the edit field.


If the [Style](./style.md) is `'Simple'` or `'DropEdit'`, the user may type text into the edit field. In these cases, the contents of the edit field may also be specified or queried using the [Text](./text.md) property.


Note that if the user first selects an item from the list box, then changes it in the edit field, the entry in the list box is automatically deselected. There is therefore no conflict between the value of [Text](Text.htm) and the value of [SelItems](./selitems.md).


**Warning: Windows truncates the contents of the edit field (reflected in the value of the Text property) to 510 characters.**


For a Combo with [Style ](./style.md)`'Simple'`, the [Index](./index.md) property specifies or reports the position of [Items](./items.md) in the list box as a positive integer value. If [Index](./index.md) has the value "n", it means that the "nth" item in [Items](./items.md) is displayed on the top line in the list box. Note that [Index](./index.md) can only be set using [`⎕WS`](../../Language/System Functions/ws.htm) and **not** by [`⎕WC`](../../Language/System Functions/wc.htm) and is ignored if all the [Items](./items.md) fit in the list box. The default value for [Index](./index.md) is `⎕IO`.


The [SelText](./seltext.md) property identifies the portion of the edit field that is highlighted. It is not applicable to a Combo with [Style ](./style.md)`'Drop'` as the user cannot enter or change data in its edit field.


The height of a Combo object with [Style ](./style.md)`'Drop'` or `'DropEdit'` is defined in a manner that is different from other objects. The height of the edit field is fixed, and is dependent only upon the size of the font. The height of the associated drop-down list box is determined by the [Rows](./rows.md) property. The first element of the [Size](./size.md) property (height) is ignored. For a Simple combo box (whose listbox is permanently displayed), the overall height is determined by the first element of [Size](./size.md). [Rows](./rows.md) is a "read-only" property.


The [VScroll](./vscroll.md) property specifies whether or not a vertical scrollbar is provided. The default value 0 means no scrollbar, setting [VScroll](./vscroll.md) to `¯1` or `¯2` specifies that the Combo has a vertical scrollbar.


If the [Style](./style.md) is `'Simple'` or `'DropEdit'`, the [HScroll](./hscroll.md) property determines whether or not the edit field may be scrolled. If [HScroll](./hscroll.md) is 0, the data is not scrollable, and the user cannot enter more characters once the field is full. If [HScroll](./hscroll.md) is `¯1` or `¯2` the field is scrollable, and there is no limit on the number of characters that can be entered. In neither case however is a horizontal scrollbar provided. If [Style](./style.md) is `'Drop'`, the user is not allowed to enter data into the edit field anyway, and the value of [HScroll](./hscroll.md) is ignored.


[VScroll](./vscroll.md) and [HScroll](./hscroll.md) may only be set when the object is created and may not subsequently be changed.


Note that when you change the [Items](./items.md) property using [`⎕WS`](../../Language/System Functions/ws.htm), the [Text](Text.htm), [SelItems](./selitems.md) and [SelText](./seltext.md) properties are all reset to their default values.


The Combo object will report a [Select](./select.md) event (if enabled) when the user chooses an item from the list box. It will generate a [Change](./change.md) event (if enabled) when the user manually alters the contents of the edit field and then changes the focus to another object.


