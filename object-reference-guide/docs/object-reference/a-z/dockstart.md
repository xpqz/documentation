




<h1 class="heading"><span class="name">DockStart</span></h1>
| Applies To: | [CoolBand](./coolband.md) | [CoolBar](./coolbar.md) | [Form](./form.md) | [SubForm](./subform.md) | [ToolControl](./toolcontrol.md) |
| --- | --- | --- | --- | --- | ---  |

| Applies To: | [CoolBand](./coolband.md) [CoolBar](./coolbar.md) [Form](./form.md) [SubForm](./subform.md) [ToolControl](./toolcontrol.md) | [CoolBand](./coolband.md) | [CoolBar](./coolbar.md) | [Form](./form.md) | [SubForm](./subform.md) | [ToolControl](./toolcontrol.md) |  |
| --- | --- | ---  |
| [CoolBand](./coolband.md) | [CoolBar](./coolbar.md) | [Form](./form.md) |
| [SubForm](./subform.md) | [ToolControl](./toolcontrol.md) |  |


Description


If enabled, this event is reported by a dockable object (one whose [Dockable](./dockable.md) property is set to 1) when the user starts to drag it using the mouse.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'DockStart'` or 480 |


A callback function may prevent the docking operation from starting by returning 0.



The associated callback is run immediately while the windows notification is still on the stack. See 
Interface Guide: 

High-Priority Callback FunctionsHigh-Priority Callback Functions on page 1.


