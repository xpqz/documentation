




<h1 class="heading"><span class="name">Menu</span></h1>

| [Parents](../ParentLists/Menu.htm) | [Children](../ChildLists/Menu.htm) | [Properties](../PropLists/Menu.htm) | [Methods](../MethodLists/Menu.htm) | [Events](../EventLists/Menu.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | This is a pop-up object which allows the user to initiate an action or         to select an option using a "menu". |
| --- | ---  |


**Description**


For a Menu that is owned by a [MenuBar](../a-z/menubar.md) or
another Menu, the [Caption](../a-z/caption.md) property
determines the text string that is displayed as the "choice". The Menu
is then popped up by the user clicking on this text. It is automatically popped
down when the user chooses an option (by selecting a [MenuItem](../a-z/menuitem.md))
or cancels the operation (by clicking elsewhere).



If a Menu belongs to a [Form](../a-z/form.md), [SubForm](../a-z/subform.md) or is a top-level object, it must be popped up by the application. This is
commonly done in response to a [MouseDown](../a-z/mousedown.md) event. A Menu is popped-up by calling [`⎕DQ`](../../Language/System Functions/dq.htm) with only the name of the Menu as its argument. The user may therefore not
interact with any other object until a selection is made or until the operation
is cancelled. When either occurs, the Menu is automatically popped down and
de-activated, and its [`⎕DQ`](../../Language/System Functions/dq.htm) terminates.


The Menu object does not have a [Size](../a-z/size.md) property. Instead, its size is determined automatically by its contents.


If a Menu is owned by a [MenuBar](../a-z/menubar.md) or by
another Menu, its position within its parent is also calculated automatically,
dependent on the order in which other related objects are established. The [Posn](../a-z/posn.md) property may however be used to **insert** a new Menu into an existing
structure. For example, having defined three Menu objects as children of a [MenuBar](../a-z/menubar.md),
you can insert a fourth one between the first and the second by specifying its [Posn](../a-z/posn.md) to be 2. Note that the value of [Posn](../a-z/posn.md) for the
Menus that were previously second and third will then be reset to 3 and 4
respectively.


If a Menu is a child of a [MenuBar](../a-z/menubar.md) which is
itself a child of a [Form](../a-z/form.md) or [SubForm](../a-z/subform.md),
the Align property can be set to `'Right'`.
This is used to position a single Menu (or [MenuItem](../a-z/menuitem.md))
at the rightmost end of a [MenuBar](../a-z/menubar.md). This does
not apply if the [MenuBar](../a-z/menubar.md) is owned by a [ToolControl](../a-z/toolcontrol.md).


The [BtnPix](../a-z/btnpix.md) property is used to display a
picture in a Menu. [BtnPix](../a-z/btnpix.md) specifies the
names of, or refs to, three [Bitmap](../a-z/bitmap.md) objects.
The first [Bitmap](../a-z/bitmap.md) is displayed when the Menu
does not have the focus (normal), the second when it does have the focus
(highlighted). The third [Bitmap](../a-z/bitmap.md) is displayed
when the Menu is made inactive ([Active](../a-z/active.md) property is 0). If [Caption](../a-z/caption.md) is also defined,
it is displayed **on top of** the bitmaps.


If the Menu is a submenu (owned by a Menu), you may set its [EdgeStyle](../a-z/edgestyle.md) property to `'Plinth'`. This causes the Menu
to take on an appearance that is similar to a pushbutton and be raised when not
selected and recessed when selected. Note that to enable 3-dimensional
appearance, you must set [EdgeStyle](../a-z/edgestyle.md) to
something other than `'None'` for all the
objects above the Menu in the tree.


[EdgeStyle](../a-z/edgestyle.md), [BtnPix](../a-z/btnpix.md),
[Font](../a-z/font.md), [FCol](../a-z/fcol.md) and
[BCol](../a-z/bcol.md) do not affect the appearance of a Menu if
it is the direct child of a [MenuBar](../a-z/menubar.md). However,
the [EdgeStyle](../a-z/edgestyle.md) property **must** be set
to something other than `'None'` if you want
its children Menu and [MenuItem](../a-z/menuitem.md) objects to
have a 3-dimensional appearance.


