




<h1 class="heading"><span class="name">TabButton</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | The TabButton object represents an individual tab or button in a [TabControl](../a-z/tabcontrol.md) |
| --- | --- | ---  |
| Parents | [Detach](../a-z/detach.md) | [Detach](../a-z/detach.md) |  |  |
| [Detach](../a-z/detach.md) |  |  |
| Children | [Detach](../a-z/detach.md) | [Detach](../a-z/detach.md) |  |  |
| [Detach](../a-z/detach.md) |  |  |
| Properties | [Detach](../a-z/detach.md) | [Detach](../a-z/detach.md) |  |  |
| [Detach](../a-z/detach.md) |  |  |
| Methods | [Detach](../a-z/detach.md) | [Detach](../a-z/detach.md) |  |  |
| [Detach](../a-z/detach.md) |  |  |
| Events | [Detach](../a-z/detach.md) | [Detach](../a-z/detach.md) |  |  |
| [Detach](../a-z/detach.md) |  |  |


Description


The TabButton object represents an individual tab or button in a [TabControl](../a-z/tabcontrol.md)



The position and size of a TabButton object are entirely determined by its parent [TabControl](../a-z/tabcontrol.md) and may not be altered. For this reason, the [Posn](../a-z/posn.md) and [Size](../a-z/size.md) properties are read-only.


The [Caption](../a-z/caption.md) property specifies the text that appears on the button or tab.


A picture is specified by setting the ImageIndex property of the TabButton. This is a number that points to a particular icon or bitmap defined in an [ImageList](../a-z/imagelist.md) object whose name is specified by the [ImageListObj](../a-z/imagelistobj.md) property of the parent [TabControl](../a-z/tabcontrol.md).


Note that all TabButton objects share the same font which is defined by the [FontObj](../a-z/fontobj.md) property of the [TabControl](../a-z/tabcontrol.md).


The foreground and background colours of the TabButton object are fixed.


When used as a tab, a TabButton is normally attached to a [SubForm](../a-z/subform.md) by the [TabObj](../a-z/tabobj.md) property of the [SubForm](../a-z/subform.md). The [TabObj](../a-z/tabobj.md) property of the TabButton itself, is a read-only property that specifies the name of, or ref to, the [SubForm](../a-z/subform.md) to which the TabButton is attached.


The [State](../a-z/state.md) property reports the (selected) state of a TabButton.


