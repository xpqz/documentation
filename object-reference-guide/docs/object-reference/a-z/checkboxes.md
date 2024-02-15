




<h1 class="heading"><span class="name">CheckBoxes</span></h1>

| Applies To: | [ListView](./listview.md) | [TreeView](./treeview.md) |
| --- | --- | ---  |


**Description**


The CheckBoxes property specifies whether or not check boxes are displayed
alongside items in a [ListView](./listview.md) or [TreeView](./treeview.md) object.



CheckBoxes is a single number with the value 0 (check boxes are not
displayed) or 1 (check boxes are displayed); the default is 0.


For a [TreeView](./treeview.md), CheckBoxes will only be
honoured if the items have pictures associated with them (via the [ImageListObj](imagelistobj.md) and [ImageIndex](imageindex.md) properties).


For a [ListView](./listview.md), CheckBoxes applies to all
settings of the [View](view.md) property.


The GetItemState method can be used to determine if a specific item in a [ListView](./listview.md) or [TreeView](./treeview.md) is checked. The result of the
method will have the 13th bit set if the item is checked.
```apl
      STATE←Form.ListView.GetItemState 11
      13⊃⌽(32⍴2)⊤STATE
1
```



The picture below illustrates the effect on the appearance of a [ListView](./listview.md) object, of setting CheckBoxes to 1.


![lv_cb](../img/lv-cb.gif)



