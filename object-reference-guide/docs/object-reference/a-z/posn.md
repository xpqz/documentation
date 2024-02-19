




<h1 class="heading"><span class="name">Posn</span></h1>

**Applies To**


**Description**


With the exception of [Menu](./menu.md), [MenuItem](./menuitem.md) and [Separator](./separator.md) objects, Posn is a 2-element numeric vector specifying the y-position and x-position respectively of the top-left corner of the object relative to its parent. For a [Form](./form.md), Posn specifies its position on the screen. The units are defined by the [Coord](coord.md) property.


When specifying Posn for [`⎕WC`](../../Language/System Functions/wc.htm), you can allow the y-position or x-position to assume a default value by giving the corresponding element a value of `⍬`.


Using [`⎕WS`](../../Language/System Functions/ws.htm), if you want to set the y-position, but not the x-position, or vice-versa, you should specify `⍬` for the item you don't want to change.


For [Menu](./menu.md), [MenuItem](./menuitem.md) and [Separator](./separator.md) objects, Posn is a single integer that specifies the position at which the object is to be **inserted** in its parent. For example, to add a new [MenuItem](./menuitem.md) between the third and fourth items in an existing [Menu](./menu.md), you would specify its Posn as 4. For these objects, the value of Posn returned by [`⎕WG`](../../Language/System Functions/wg.htm) is the current index of the object within its parent.



