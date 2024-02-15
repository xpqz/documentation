




<h1 class="heading"><span class="name">MDITile</span></h1>

| Applies To: | [MDIClient](../a-z/mdiclient.md) |
| --- | ---  |


**Description**


This method causes the [MDIClient](../a-z/mdiclient.md) object
to organise its child [Form](../a-z/form.md)s as a row or column.
To permit the user to carry out this action, it is recommended that a suitable
callback function or expression is attached to a [MenuItem](../a-z/menuitem.md) or [Button](../a-z/button.md). The callback function or expression
should then call the MDITile method.


Note that because there are restrictions concerning the minimum height and
width of a window, MS-Windows does not necessarily respond as requested. If the [MDIClient](../a-z/mdiclient.md) is itself of insufficient size, or if it contains a large number of child [Form](../a-z/form.md)s,
Windows may choose to tile the [Form](../a-z/form.md)s in a row
when a column was specified or vice versa. It may also choose to ignore the
event entirely.


The argument to MDITile is `⍬`, or
a single item as follows:


| `[1]` | Tile Mode | 0 (vertical) 1 (horizontal) |
| --- | --- | ---  |


If the argument is `⍬`, the *Tile Mode* defaults to 0.



