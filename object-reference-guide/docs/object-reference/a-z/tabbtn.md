




<h1 class="heading"><span class="name">TabBtn</span></h1>

| [Parents](../ParentLists/TabBtn.htm) | [Children](../ChildLists/TabBtn.htm) | [Properties](../PropLists/TabBtn.htm) | [Methods](../MethodLists/TabBtn.htm) | [Events](../EventLists/TabBtn.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | To tab a [SubForm](subform.md) . |
| --- | ---  |


**Description**


TabBtn objects are associated with [SubForm](subform.md)s which are positioned on top of one another. When the user clicks on a TabBtn, the corresponding [SubForm](subform.md) is brought to the top and given the focus.



[TabBar](TabBar.htm) and TabBtn objects were implemented before Windows provided direct support for tabbed dialogs, and have been superceded by [TabControl](TabControl.htm) and [TabButton](TabButton.htm) objects. Please use these instead.


The appearance of a TabBtn is determined by its [EdgeStyle](./edgestyle.md), [Border](./border.md) and [Caption](./caption.md) properties. These take their defaults from the [SubForm](subform.md) with which the TabBtn is associated. Thus there is generally no need to specify them. [BCol](./bcol.md) also defaults to that of its associated [SubForm](subform.md).


The position of a TabBtn is normally determined by its parent [TabBar](TabBar.htm) and its default size is fixed (22 x 80 pixels), and not related to the size of its [Caption](./caption.md). These defaults can be overridden using the [Posn](./posn.md) and [Size](./size.md) properties.


A [SubForm](subform.md) is associated with a TabBtn by setting the [TabObj](./tabobj.md) property of the [*SubForm*](subform.md) to the name of, or ref to, the TabBtn. The [TabObj](./tabobj.md) property of the TabBtn is a read-only property that contains the name of, or ref to, the associated [SubForm](subform.md).


