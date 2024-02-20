




<h1 class="heading"><span class="name">Separator</span></h1>

[Parents](../ParentLists/Separator.htm) [Children](../ChildLists/Separator.htm) [Properties](../PropLists/Separator.htm) [Methods](../MethodLists/Separator.htm) [Events](../EventLists/Separator.htm)


Purpose: A horizontal or vertical line used to separate items in a menu.


**Description**


This object provides a vertical or horizontal line to separate items in a [Menu](../a-z/menu.md). It may also be used to split a [MenuBar](../a-z/menubar.md) over more than one line.



The orientation of the Separator is determined by its [Style](../a-z/style.md) property, which may be `'Horz'` (horizontal) or `'Vert'` (vertical). The default is `'Horz'`.


If you want to provide a menu with a 3-Dimensional (pushbutton) appearance, you should also set the [EdgeStyle](../a-z/edgestyle.md) property on any Separator objects in it. Alternatively, you can achieve the same effect by setting the background colour ([BCol](../a-z/bcol.md)) for the Separators to grey (192 192 192).


The [Posn](../a-z/posn.md) property is a single integer number which specifies the positional index of the Separator relative to the other objects in the [Menu](../a-z/menu.md). A Separator does not generate any events.


Like other components of a menu, the position of a Separator is normally determined by the order in which it is created in relation to other objects with the same parent. However, you can use the [Posn](../a-z/posn.md) property to **insert** a Separator into an existing structure. For example, having defined three [MenuItem](../a-z/menuitem.md) objects as children of a [Menu](../a-z/menu.md), you can insert a Separator between the first and the second by specifying its [Posn](../a-z/posn.md) to be 2. Note that the value of [Posn](../a-z/posn.md) for the [MenuItem](../a-z/menuitem.md)s that were previously second and third will then be reset to third and fourth respectively.


If you put a Separator (either [Style](../a-z/style.md)) into a [MenuBar](../a-z/menubar.md), it has the effect of adding another line to it. Any items added after the Separator will appear in the new line.


