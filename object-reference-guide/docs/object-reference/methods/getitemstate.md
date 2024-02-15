




<h1 class="heading"><span class="name">GetItemState</span></h1>

| Applies To: | [ListView](../a-z/listview.md) | [TreeView](../a-z/treeview.md) |
| --- | --- | ---  |


**Description**


This method is used to obtain the status of a particular item in a [ListView](../a-z/listview.md) or [TreeView](../a-z/treeview.md) object.


The argument for GetItemState is a single item as follows:


| `[1]` | Item number | Integer |
| --- | --- | ---  |


*Item number* is the index of the item concerned. Be aware that this is index origin dependent.


The result indicates the state of the item as the sum of one or more of the following codes:



| `¯1` | Error (most likely the Item number is invalid) |
| --- | ---  |
| 1 | Item has the focus |
| 2 | Item is selected |
| 8 | Item is highlighted for dropping |
| 16 | Item is displayed in bold text |
| 32 | Item is expanded |
| 64 | Item is or has been expanded |
| 4096 | Item is checked. See "CheckBoxes" on page 1 |


