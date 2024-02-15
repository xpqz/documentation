




<h1 class="heading"><span class="name">GetTipText</span></h1>

| Applies To: | [ListView](./listview.md) | [TreeView](./treeview.md) |
| --- | --- | ---  |


**Description**


If enabled, this event is reported by a [TreeView](./treeview.md) or [ListView](./listview.md) object just before it displays a tip for a specific row.


The event message reported as the result of `⎕DQ`, or supplied as the right argument to your callback function, is a 5-element vector as follows :


| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'GetTipText'` or 325 |
| `[3]` | Item index | Integer ( `⎕IO` dependent) |
| `[4]` | SubItem index | Integer ( `⎕IO` dependent, currently always equal to `⎕IO` ) |
| `[5]` | TipText | The text to be displayed. |


Modifying and returning the 5th element of the argument to the callback function allows the application to change the displayed tip.


The text can be set to a character array of rank 2 or less.


The default processing for the event is to display the default tip (if there is one).



The associated callback is run **immediately** while the windows notification is still on the stack. See 
Interface Guide: 

High-Priority Callback FunctionsHigh-Priority Callback Functions on page 1.


