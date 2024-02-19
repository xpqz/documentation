




<h1 class="heading"><span class="name">FileBoxCancel</span></h1>

| Applies To: | [BrowseBox](../a-z/browsebox.md) | [FileBox](../a-z/filebox.md) |
| --- | --- | ---  |


**Description**


If enabled, this event is reported when a [FileBox](../a-z/filebox.md) is closed because the user has pressed the "Cancel" button or closed it.


The event message reported as the result of [`⎕DQ`](../../Language/System Functions/dq.htm), or supplied as the right argument to your callback function, is a 3-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'FileBoxCancel'` or 72 |
| `[3]` | File name | character vector containing the name of the currently selected file (empty if none) |



