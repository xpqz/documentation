



<h1 class="heading"><span class="name">Retracting</span></h1>

Applies To: [Grid](../a-z/grid.md) [TreeView](../a-z/treeview.md)


**Description**


If enabled, this event is reported by a [Grid](../a-z/grid.md) or a [TreeView](../a-z/treeview.md) object just before it is about to retract to hide the children of the current item.


In a [Grid](../a-z/grid.md), this occurs when the user clicks the picture or tree line in the row title.


In a [TreeView](../a-z/treeview.md), this occurs when the user double-clicks the item label or clicks in the button or on the tree line to the left of the item label, when the item is in its expanded state.


The default processing for the event is to retract the tree at the corresponding point.


You may disable the retract operation by setting the action code for the event to `¯1`. You may also prevent the retraction from occurring by returning 0 from a callback function. You may retract [Grid](../a-z/grid.md) a or a [TreeView](../a-z/treeview.md) dynamically under program control by calling Retracting as a method.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 3-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'Retracting'` or 304 |
| `[3]` | Item number | Integer. The index of the item. |


