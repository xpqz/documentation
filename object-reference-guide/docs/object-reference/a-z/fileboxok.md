




<h1 class="heading"><span class="name">FileBoxOK</span></h1>

Applies To: [BrowseBox](./browsebox.md) [FileBox](./filebox.md)


**Description**


If enabled, this event is reported when a [FileBox](./filebox.md) is closed because the user has pressed the "Open" or "Save" button.


The event message reported as the result of [`⎕DQ`](../../Language/System Functions/dq.htm), or supplied as the right argument to your callback function, is a 3-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'FileBoxOK'` or 71 |
| `[3]` | File name | character vector containing the name of the currently selected file (empty if none) |



