




<h1 class="heading"><span class="name">EditLabels</span></h1>

| Applies To: | [ListView](./listview.md) | [TreeView](./treeview.md) |
| --- | --- | ---  |


**Description**


The EditLabels property is Boolean and specifies whether or not the labels (specified by the Items property) in a [ListView](./listview.md) or [TreeView](./treeview.md) object may be edited by the user. Its default value is 0 (editing is not allowed).


If EditLabels is 1, the user begins editing by clicking the label of the item that has the focus. This causes a pop-up edit box to appear around the item and allows the use to change it. A [BeginEditLabel](./begineditlabel.md) event is reported at the start of the edit operation and an [EndLabelEdit](./endeditlabel.md) event is reported on its completion. You may control the edit of a particular label using callback functions attached to these events.



