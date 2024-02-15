




<h1 class="heading"><span class="name">TabObj</span></h1>
| Applies To: | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) | [TabButton](./tabbutton.md) | [TabControl](./tabcontrol.md) |
| --- | --- | --- | --- | --- | ---  |

| Applies To: | [SubForm](./subform.md) [TabBar](./tabbar.md) [TabBtn](./tabbtn.md) [TabButton](./tabbutton.md) [TabControl](./tabcontrol.md) | [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) | [TabButton](./tabbutton.md) | [TabControl](./tabcontrol.md) |  |
| --- | --- | ---  |
| [SubForm](./subform.md) | [TabBar](./tabbar.md) | [TabBtn](./tabbtn.md) |
| [TabButton](./tabbutton.md) | [TabControl](./tabcontrol.md) |  |


Description


TabObj is a ref or a character vector.


TabObj associates a [SubForm](./subform.md) with a [TabBtn](./tabbtn.md) or a [TabButton](./tabbutton.md) object. Selecting the associated [TabBtn](./tabbtn.md) or [TabButton](./tabbutton.md) causes the [SubForm](./subform.md) to be given the input focus.


For a [SubForm](./subform.md), it specifies the name of, or ref to, a [TabBtn](./tabbtn.md) or [TabButton](./tabbutton.md) object that is to be associated with the [SubForm](./subform.md). When referenced or queried using `⎕WG`, TabObj returns a name if it was specified by a name, or a ref if it was specified by a ref.


For [TabBtn](./tabbtn.md) and [TabButton](./tabbutton.md) objects, TabObj is a read-only property that contains a ref to the associated [SubForm](./subform.md).


For a [TabBar](./tabbar.md) or [TabControl](./tabcontrol.md), TabObj is a read-only property that contains a ref to the currently selected [TabBtn](./tabbtn.md) or [TabButton](./tabbutton.md).



