




<h1 class="heading"><span class="name">SubForm</span></h1>

| [Parents](../ParentLists/SubForm.htm) | [Children](../ChildLists/SubForm.htm) | [Properties](../PropLists/SubForm.htm) | [Methods](../MethodLists/SubForm.htm) | [Events](../EventLists/SubForm.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | This object represents a window that is owned by and constrained         within another [Form](Form.htm) or an [MDIClient](MDIClient.htm) . |
| --- | ---  |


**Description**


If the SubForm is the child of a [Form](Form.htm), it is
by default a simple featureless window that occupies the entire client area
(excluding standard [ToolBar](toolbar.md)s, [StatusBar](StatusBar.htm)s
and [TabBar](TabBar.htm)s) of its parent.



The properties
that control its appearance, including [Sizeable](./sizeable.md),
[Moveable](./moveable.md), [SysMenu](./sysmenu.md),
[Border](./border.md), [MaxButton](./maxbutton.md) and [MinButton](./minbutton.md), all default to 0. The [EdgeStyle](./edgestyle.md) property also defaults to `'None'`, so the
background of the SubForm defaults to the Window Background colour.


If the SubForm is the child of an [MDIClient](MDIClient.htm),
its default appearance is the same as for a top-level [Form](Form.htm).
By default its size is 25% of its parent client area and it is positioned in the
centre of its parent object.


The [Posn](./posn.md) property specifies the location of
the **internal** top-left corner of the SubForm relative to its parent. If
the SubForm has a title bar, border, or a 3-dimensional shadow, you must allow
sufficient space for these components. Similarly, the [Size](./size.md) property specifies the internal size of the SubForm excluding the title bar and
border.


A SubForm is constrained so that it cannot be moved outside its parent. In
all other respects it behaves in a similar manner to a [Form](Form.htm) object. See [Form](Form.htm) object and the descriptions of
its properties for further details.


