




<h1 class="heading"><span class="name">DockCancel</span></h1>
| Applies To: | [CoolBand](../a-z/coolband.md) | [CoolBar](../a-z/coolbar.md) | [Form](../a-z/form.md) | [SubForm](../a-z/subform.md) | [ToolControl](../a-z/toolcontrol.md) |
| --- | --- | --- | --- | --- | ---  |

| Applies To: | [CoolBand](../a-z/coolband.md) [CoolBar](../a-z/coolbar.md) [Form](../a-z/form.md) [SubForm](../a-z/subform.md) [ToolControl](../a-z/toolcontrol.md) | [CoolBand](../a-z/coolband.md) | [CoolBar](../a-z/coolbar.md) | [Form](../a-z/form.md) | [SubForm](../a-z/subform.md) | [ToolControl](../a-z/toolcontrol.md) |  |
| --- | --- | ---  |
| [CoolBand](../a-z/coolband.md) | [CoolBar](../a-z/coolbar.md) | [Form](../a-z/form.md) |
| [SubForm](../a-z/subform.md) | [ToolControl](../a-z/toolcontrol.md) |  |


Description


If enabled, this event is reported by a client object when the user aborts a docking operation by pressing Escape.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'DockCancel'` or 485 |


This event is reported for information only and cannot be cancelled or inhibited in any way.



The associated callback is run immediately while the windows notification is still on the stack. See 
Interface Guide: 

High-Priority Callback FunctionsHigh-Priority Callback Functions on page 1.

