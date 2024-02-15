




<h1 class="heading"><span class="name">MenuItem</span></h1>

| [Parents](../ParentLists/MenuItem.htm) | [Children](../ChildLists/MenuItem.htm) | [Properties](../PropLists/MenuItem.htm) | [Methods](../MethodLists/MenuItem.htm) | [Events](../EventLists/MenuItem.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | This object allows the user to initiate an action or to select an option from a menu. |
| --- | ---  |


**Description**


The [Caption](./caption.md) property determines the text string that is displayed in its parent as the menu option. The size of a MenuItem is determined by the size of its [Caption](./caption.md), or by the size of the largest object ([Menu](menu.md), MenuItem or [Separator](separator.md)) with the same parent. The position of the MenuItem is normally determined by the order in which it is created in relation to other objects with the same parent. However, you can use the [Posn](./posn.md) property to **insert** a new MenuItem into an existing structure. For example, having defined three MenuItem objects as children of a [Menu](menu.md), you can insert a fourth one between the first and the second by specifying its [Posn](./posn.md) to be 2. Note that the value of [Posn](./posn.md) for the MenuItems that were previously second and third will then be reset to 3 and 4 respectively.



The [Style](./style.md) property may be `'Check'` (the default) or `'Radio'`. [Style](./style.md) determines the type of graphic displayed alongside the Caption if the MenuItem is *checked*.


The [Checked](./checked.md) property is a single number with the value 0 or 1. 0 means not checked (the default), 1 means checked and a tick mark or radio dot is placed alongside its [Caption](./caption.md). This property is frequently used to indicate which of a choice of options is currently set.


If a MenuItem is a child of a [MenuBar](menubar.md) which is itself a child of a [Form](form.md) or [SubForm](subform.md), the Align property can be set to `'Right'`. This is used to position a single MenuItem (or [Menu](menu.md)) at the rightmost end of a [MenuBar](menubar.md). This does not apply if the [MenuBar](menubar.md) is owned by a [ToolControl](toolcontrol.md).


If you set the [EdgeStyle](./edgestyle.md) property to `'Plinth'`, the MenuItem will take on an appearance that is similar to a pushbutton and be raised when not selected and recessed when selected. Note that to enable 3-dimensional appearance, you must set [EdgeStyle](./edgestyle.md) to something other than `'None'` for all the objects above the MenuItem in the tree.


The [BtnPix](./btnpix.md) property is used to display a picture in a MenuItem. [BtnPix](./btnpix.md) specifies the names of, or refs to, three [Bitmap](bitmap.md) objects. The first [Bitmap](bitmap.md) is displayed when the MenuItem does not have the focus (normal), the second when it does have the focus (highlighted). The third [Bitmap](bitmap.md) is displayed when the MenuItem is made inactive ([Active](./active.md) property is 0). If [Caption](./caption.md) is also defined, it is displayed **on top of** the bitmaps.


Alternatively, you may display an image alongside the [Caption](./caption.md) using the [ImageIndex](./imageindex.md) property. This selects a picture from the [ImageList](imagelist.md) associated with the [ImageListObj](./imagelistobj.md) property of the parent [Menu](menu.md).


[EdgeStyle](./edgestyle.md), [BtnPix](./btnpix.md), [FontObj](./fontobj.md), [FCol](./fcol.md) and [BCol](./bcol.md) are not effective if the MenuItem is the direct child of a [MenuBar](menubar.md).


A MenuItem generates a [Select](./select.md) event (if enabled) when the user chooses it.


