




<h1 class="heading"><span class="name">BalloonHide</span></h1>

| Applies To: | [SysTrayItem](./systrayitem.md) |
| --- | ---  |


**Description**


If enabled, this event is reported by an [SysTrayItem](./systrayitem.md) object when a BalloonTip disappears for any reason other than it is dismissed by a timeout or because the user clicked the mouse.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'BalloonHide'` or 862 |


This event is reported for information only and cannot be disabled or modified in any way



