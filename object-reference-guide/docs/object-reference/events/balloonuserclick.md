




<h1 class="heading"><span class="name">BalloonUserClick</span></h1>

Applies To: [SysTrayItem](../a-z/systrayitem.md)


**Description**


If enabled, this event is reported by an [SysTrayItem](../a-z/systrayitem.md) object when a BalloonTip is dismissed because the user clicked the mouse in the body of the BalloonTip. It is not reported when the user clicks the **close** (X) button.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 2-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'BalloonUserClick'` or 864 |


This event is reported for information only and cannot be disabled or modified in any way



