




<h1 class="heading"><span class="name">TabBar</span></h1>

| [Parents](../ParentLists/TabBar.htm) | [Children](../ChildLists/TabBar.htm) | [Properties](../PropLists/TabBar.htm) | [Methods](../MethodLists/TabBar.htm) | [Events](../EventLists/TabBar.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | To manage a set of [TabBtn](../a-z/tabbtn.md) objects. |
| --- | ---  |


**Description**


The TabBar object manages a group of [TabBtn](../a-z/tabbtn.md) objects. These are associated with a set of [SubForm](../a-z/subform.md) objects which are positioned on top of one another. When the user clicks on a [TabBtn](../a-z/tabbtn.md),
the corresponding [SubForm](../a-z/subform.md) is brought to the
top and given the focus.



TabBar and [TabBtn](../a-z/tabbtn.md) objects were implemented
before Windows provided direct support for tabbed dialogs, and have been
superceded by [TabControl](../a-z/tabcontrol.md) and [TabButton](../a-z/tabbutton.md) objects. Please use these instead.


By default, a TabBar is a flat bar stretched across the bottom of its parent
form. You can alter its appearance using its [EdgeStyle](../a-z/edgestyle.md) property and you can control its alignment with its [Align](../a-z/align.md) property. [Align](../a-z/align.md) can be set to Top, Bottom
(the default), Left or Right and causes the TabBar to be attached to the
corresponding edge of the [Form](../a-z/form.md). A TabBar aligned
Top or Bottom will automatically stretch or shrink horizontally when its parent [Form](../a-z/form.md) is resized, but it will remain fixed vertically. A TabBar aligned Left or Right
will stretch vertically but will remain fixed horizontally. By default a TabBar
occupies the entire width or length of the side of the [Form](../a-z/form.md) to which it is attached. Both the [Posn](../a-z/posn.md) and [Size](../a-z/size.md) properties can be altered.


The alignment of a TabBar also determines the orientation of its [TabBtn](../a-z/tabbtn.md)s.
TabBars aligned Top or Bottom cause their [TabBtn](../a-z/tabbtn.md)s
to be drawn left to right with the free edge of the [TabBtn](../a-z/tabbtn.md)s
facing downwards or upwards respectively. TabBar aligned Left or Right draw
their [TabBtn](../a-z/tabbtn.md)s downwards with their free edges
facing left or right respectively.


By default, [TabBtn](../a-z/tabbtn.md) objects are positioned
along the inner edge of the TabBar. This is the edge closest to the [SubForm](../a-z/subform.md) s they will tab. They are also positioned so that they overlap one another
horizontally or vertically according to the [Align](../a-z/align.md) property.


The [HScroll](../a-z/hscroll.md) and [VScroll](../a-z/vscroll.md) properties determine what happens when the end of the TabBar is reached. If [HScroll](../a-z/hscroll.md) or [VScroll](../a-z/vscroll.md) is 0 (the default) a [TabBtn](../a-z/tabbtn.md) that would otherwise extend beyond the TabBar is instead positioned immediately
above, below or alongside the first [TabBtn](../a-z/tabbtn.md) in
the TabBar, thereby starting a new row or column. Note however that the TabBar
is not automatically resized vertically to accommodate a second row or column.
If you want a multi-flight TabBar you have to set its height or width
explicitly. If [HScroll](../a-z/hscroll.md) or [VScroll](../a-z/vscroll.md) is `¯1` or `¯2`,
[TabBtn](../a-z/tabbtn.md)s continue to be added along the TabBar
even though they extend beyond its boundary and may be scrolled into view using
a mini scrollbar. If [HScroll](../a-z/hscroll.md) is `¯1`,
the scrollbar is shown whether or not any controls extend beyond the TabBar. If [HScroll](../a-z/hscroll.md) is `¯2`, the scrollbar appears only if
required and may appear or disappear when the user resizes the parent [Form](../a-z/form.md).


[VScroll](../a-z/vscroll.md) and [HScroll](../a-z/hscroll.md) may only be set when the object is created and may not subsequently be changed.


If you specify a value for its [Posn](../a-z/posn.md) property, a [TabBtn](../a-z/tabbtn.md) will be placed at the
requested position regardless of the value of [Style](../a-z/style.md),
[HScroll](../a-z/hscroll.md) or [VScroll](../a-z/vscroll.md).
However, the next control added will take its default position from the previous
one according to the value of these properties. Thus if you wish to group your
controls together with spaces between the groups, you need only specify the
position of the first one in each group.


If you specify a value for its [Posn](../a-z/posn.md) property, a [TabBtn](../a-z/tabbtn.md) will be placed at the
requested position regardless of the value of [Align](../a-z/align.md).
However, the next [TabBtn](../a-z/tabbtn.md) added will take its
default position from the previous one. Thus if you wish to group your [TabBtn](../a-z/tabbtn.md)s
together with spaces between the groups, you need only specify the position of
the first one in each group.


