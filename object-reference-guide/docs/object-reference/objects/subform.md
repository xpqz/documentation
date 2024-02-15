




<h1 class="heading"><span class="name">SubForm</span></h1>

| [Parents](../ParentLists/SubForm.htm) | [Children](../ChildLists/SubForm.htm) | [Properties](../PropLists/SubForm.htm) | [Methods](../MethodLists/SubForm.htm) | [Events](../EventLists/SubForm.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | This object represents a window that is owned by and constrained         within another [Form](../a-z/form.md) or an [MDIClient](../a-z/mdiclient.md) . |
| --- | ---  |


**Description**


If the SubForm is the child of a [Form](../a-z/form.md), it is
by default a simple featureless window that occupies the entire client area
(excluding standard [ToolBar](../a-z/toolbar.md)s, [StatusBar](../a-z/statusbar.md)s
and [TabBar](../a-z/tabbar.md)s) of its parent.



The properties
that control its appearance, including [Sizeable](../a-z/sizeable.md),
[Moveable](../a-z/moveable.md), [SysMenu](../a-z/sysmenu.md),
[Border](../a-z/border.md), [MaxButton](../a-z/maxbutton.md) and [MinButton](../a-z/minbutton.md), all default to 0. The [EdgeStyle](../a-z/edgestyle.md) property also defaults to `'None'`, so the
background of the SubForm defaults to the Window Background colour.


If the SubForm is the child of an [MDIClient](../a-z/mdiclient.md),
its default appearance is the same as for a top-level [Form](../a-z/form.md).
By default its size is 25% of its parent client area and it is positioned in the
centre of its parent object.


The [Posn](../a-z/posn.md) property specifies the location of
the **internal** top-left corner of the SubForm relative to its parent. If
the SubForm has a title bar, border, or a 3-dimensional shadow, you must allow
sufficient space for these components. Similarly, the [Size](../a-z/size.md) property specifies the internal size of the SubForm excluding the title bar and
border.


A SubForm is constrained so that it cannot be moved outside its parent. In
all other respects it behaves in a similar manner to a [Form](../a-z/form.md) object. See [Form](../a-z/form.md) object and the descriptions of
its properties for further details.


