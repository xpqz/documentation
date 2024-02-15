




<h1 class="heading"><span class="name">TabBtn</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | To tab a [SubForm](../a-z/subform.md) . |
| --- | --- | ---  |
| Parents | [Detach](../a-z/detach.md) [ChooseFont](../a-z/choosefont.md) | [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| Children | [Detach](../a-z/detach.md) [ChooseFont](../a-z/choosefont.md) | [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| Properties | [Detach](../a-z/detach.md) [ChooseFont](../a-z/choosefont.md) | [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| Methods | [Detach](../a-z/detach.md) [ChooseFont](../a-z/choosefont.md) | [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| Events | [Detach](../a-z/detach.md) [ChooseFont](../a-z/choosefont.md) | [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |
| [Detach](../a-z/detach.md) | [ChooseFont](../a-z/choosefont.md) |  |


Description


TabBtn objects are associated with [SubForm](../a-z/subform.md)s which are positioned on top of one another. When the user clicks on a TabBtn, the corresponding [SubForm](../a-z/subform.md) is brought to the top and given the focus.



[TabBar](../a-z/tabbar.md) and TabBtn objects were implemented before Windows provided direct support for tabbed dialogs, and have been superceded by [TabControl](../a-z/tabcontrol.md) and [TabButton](../a-z/tabbutton.md) objects. Please use these instead.


The appearance of a TabBtn is determined by its [EdgeStyle](../a-z/edgestyle.md), [Border](../a-z/border.md) and [Caption](../a-z/caption.md) properties. These take their defaults from the [SubForm](../a-z/subform.md) with which the TabBtn is associated. Thus there is generally no need to specify them. [BCol](../a-z/bcol.md) also defaults to that of its associated [SubForm](../a-z/subform.md).


The position of a TabBtn is normally determined by its parent [TabBar](../a-z/tabbar.md) and its default size is fixed (22 x 80 pixels), and not related to the size of its [Caption](../a-z/caption.md). These defaults can be overridden using the [Posn](../a-z/posn.md) and [Size](../a-z/size.md) properties.


A [SubForm](../a-z/subform.md) is associated with a TabBtn by setting the [TabObj](../a-z/tabobj.md) property of the [*SubForm*](../a-z/subform.md) to the name of, or ref to, the TabBtn. The [TabObj](../a-z/tabobj.md) property of the TabBtn is a read-only property that contains the name of, or ref to, the associated [SubForm](../a-z/subform.md).


