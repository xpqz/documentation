




<h1 class="heading"><span class="name">MenuItem</span></h1>

[Parents](../ParentLists/MenuItem.htm) [Children](../ChildLists/MenuItem.htm) [Properties](../PropLists/MenuItem.htm) [Methods](../MethodLists/MenuItem.htm) [Events](../EventLists/MenuItem.htm)


Purpose: This object allows the user to initiate an action or to select an option from a menu.


**Description**


The [Caption](../a-z/caption.md) property determines the text string that is displayed in its parent as the menu option. The size of a MenuItem is determined by the size of its [Caption](../a-z/caption.md), or by the size of the largest object ([Menu](../a-z/menu.md), MenuItem or [Separator](../a-z/separator.md)) with the same parent. The position of the MenuItem is normally determined by the order in which it is created in relation to other objects with the same parent. However, you can use the [Posn](../a-z/posn.md) property to **insert** a new MenuItem into an existing structure. For example, having defined three MenuItem objects as children of a [Menu](../a-z/menu.md), you can insert a fourth one between the first and the second by specifying its [Posn](../a-z/posn.md) to be 2. Note that the value of [Posn](../a-z/posn.md) for the MenuItems that were previously second and third will then be reset to 3 and 4 respectively.



The [Style](../a-z/style.md) property may be `'Check'` (the default) or `'Radio'`. [Style](../a-z/style.md) determines the type of graphic displayed alongside the Caption if the MenuItem is *checked*.


The [Checked](../a-z/checked.md) property is a single number with the value 0 or 1. 0 means not checked (the default), 1 means checked and a tick mark or radio dot is placed alongside its [Caption](../a-z/caption.md). This property is frequently used to indicate which of a choice of options is currently set.


If a MenuItem is a child of a [MenuBar](../a-z/menubar.md) which is itself a child of a [Form](../a-z/form.md) or [SubForm](../a-z/subform.md), the Align property can be set to `'Right'`. This is used to position a single MenuItem (or [Menu](../a-z/menu.md)) at the rightmost end of a [MenuBar](../a-z/menubar.md). This does not apply if the [MenuBar](../a-z/menubar.md) is owned by a [ToolControl](../a-z/toolcontrol.md).


If you set the [EdgeStyle](../a-z/edgestyle.md) property to `'Plinth'`, the MenuItem will take on an appearance that is similar to a pushbutton and be raised when not selected and recessed when selected. Note that to enable 3-dimensional appearance, you must set [EdgeStyle](../a-z/edgestyle.md) to something other than `'None'` for all the objects above the MenuItem in the tree.


The [BtnPix](../a-z/btnpix.md) property is used to display a picture in a MenuItem. [BtnPix](../a-z/btnpix.md) specifies the names of, or refs to, three [Bitmap](../a-z/bitmap.md) objects. The first [Bitmap](../a-z/bitmap.md) is displayed when the MenuItem does not have the focus (normal), the second when it does have the focus (highlighted). The third [Bitmap](../a-z/bitmap.md) is displayed when the MenuItem is made inactive ([Active](../a-z/active.md) property is 0). If [Caption](../a-z/caption.md) is also defined, it is displayed **on top of** the bitmaps.


Alternatively, you may display an image alongside the [Caption](../a-z/caption.md) using the [ImageIndex](../a-z/imageindex.md) property. This selects a picture from the [ImageList](../a-z/imagelist.md) associated with the [ImageListObj](../a-z/imagelistobj.md) property of the parent [Menu](../a-z/menu.md).


[EdgeStyle](../a-z/edgestyle.md), [BtnPix](../a-z/btnpix.md), [FontObj](../a-z/fontobj.md), [FCol](../a-z/fcol.md) and [BCol](../a-z/bcol.md) are not effective if the MenuItem is the direct child of a [MenuBar](../a-z/menubar.md).


A MenuItem generates a [Select](../a-z/select.md) event (if enabled) when the user chooses it.


