




<h1 class="heading"><span class="name">DeleteItems</span></h1>
| Applies To: | [TreeView](./treeview.md) |
| --- | ---  |

| Applies To: | [TreeView](./treeview.md) | [TreeView](./treeview.md) |  |  |
| --- | --- | ---  |
| [TreeView](./treeview.md) |  |  |


Description


This method is used to delete items from a [TreeView](./treeview.md) object.


The argument to DeleteItems is a 2-element array as follows:

| `[1]` | Item number | Integer. |
| --- | --- | ---  |
| `[2]` | Number of Items | Integer. |


*Item number* specifies the index of the first item to be removed.


*Number of items* specifies the number of items to be removed and refers to those items *at the same level* in the [TreeView](./treeview.md) hierarchy as the *Item number*. *Number of items* is optional and defaults to 1.


Note that any children of these items will also be removed.


The result is an integer that indicates the total number of items, including children, that have been removed from the [TreeView](./treeview.md).



