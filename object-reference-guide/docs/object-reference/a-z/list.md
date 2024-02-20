




<h1 class="heading"><span class="name">List</span></h1>

[Parents](../ParentLists/List.htm) [Children](../ChildLists/List.htm) [Properties](../PropLists/List.htm) [Methods](../MethodLists/List.htm) [Events](../EventLists/List.htm)


Purpose: Allows the user to select one or more items from a list.


**Description**


The [Items](./items.md) property is either a vector of character vectors or a character matrix, and determines the items in the List.



The size and position of the area used to display the list is defined by [Size](./size.md) and [Posn](./posn.md). If [Size](./size.md) is not chosen to represent an exact number of lines of text, the bottom line of text may be clipped.


The [Index](./index.md) property specifies or reports the position of [Items](./items.md) in the list box as a positive integer value. If [Index](./index.md) has the value "n", it means that the "nth" item in [Items](./items.md) is displayed on the top line in the list box. However, it is ignored if all the [Items](./items.md) fit within the List object. Note that [Index](./index.md) can only be set using [`⎕WS`](../../Language/System Functions/ws.htm) and not by [`⎕WC`](../../Language/System Functions/wc.htm). The default value for [Index](./index.md) is `⎕IO`.


The [Style](./style.md) property may be `'Single'` (the default) or `'Multi'`. `'Single'` allows only a single item to be selected. `'Multi'` allows several items to be chosen. In either case, if the [Select](./select.md) event is enabled, it is generated whenever the selection changes. If [Style](./style.md) is `'Multi'` the List will generate a [Select](./select.md) event every time an item is added to the selected list.


Under Windows, you may select or de-select multiple items in a List object by pressing the Ctrl key at the same time as pressing the left mouse button.


The [SelItems](./selitems.md) property is a Boolean vector with one element per element or row in [Items](./items.md) and indicates which (if any) of the items is currently selected (and highlighted).


The [VScroll](./vscroll.md) property determines whether or not the list has a scrollbar. Its possible values are :


| `¯2` | scrollbar if required |
| --- | ---  |
| `¯1` | scrollbar if required |
| `0` | no scrollbar |


Note that data in a List is always scrollable if there are more items than will fit in the box. [VScroll](./vscroll.md) determines ONLY whether or not a scrollbar is provided.


The [MultiColumn](./multicolumn.md) property is a Boolean value that specifies whether or not the List object displays its items in columns. The default is 0 which produces a single-column display. If [MultiColumn](./multicolumn.md) is 1, the List object displays its items in columns whose width is defined by the [ColumnWidth](./columnwidth.md) property.


