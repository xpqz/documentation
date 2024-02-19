




<h1 class="heading"><span class="name">MultiLine</span></h1>

| Applies To: | [TabControl](./tabcontrol.md) | [ToolControl](./toolcontrol.md) |
| --- | --- | ---  |


**Description**


The MultiLine property determines whether or not the tabs or buttons will be arranged in multiple flights or multiple rows/columns in a [TabControl](./tabcontrol.md) or [ToolControl](./toolcontrol.md) object.


MultiLine is a single number with the value 0 (single flight of tabs, or single row/column of buttons) or 1 (multiple flights of tabs or multiple rows/columns of buttons); the default is 0.


If MultiLine is 0 and there are more tabs or buttons than will fit in the space provided, the [TabControl](./tabcontrol.md) displays an UpDown which allows the user to scroll.


However, If MultiLine is 0 in a [ToolControl](./toolcontrol.md), the buttons are clipped, and the user may have to resize the object to see them all.


See also: [Justify](Justify.htm), [TabSize](TabSize.htm).



