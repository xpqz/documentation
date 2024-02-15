




<h1 class="heading"><span class="name">CheckBoxes</span></h1>

| Applies To: | [ListView](../a-z/listview.md) | [TreeView](../a-z/treeview.md) |
| --- | --- | ---  |


**Description**


The CheckBoxes property specifies whether or not check boxes are displayed
alongside items in a [ListView](../a-z/listview.md) or [TreeView](../a-z/treeview.md) object.



CheckBoxes is a single number with the value 0 (check boxes are not
displayed) or 1 (check boxes are displayed); the default is 0.


For a [TreeView](../a-z/treeview.md), CheckBoxes will only be
honoured if the items have pictures associated with them (via the [ImageListObj](../a-z/imagelistobj.md) and [ImageIndex](../a-z/imageindex.md) properties).


For a [ListView](../a-z/listview.md), CheckBoxes applies to all
settings of the [View](../a-z/view.md) property.


The GetItemState method can be used to determine if a specific item in a [ListView](../a-z/listview.md) or [TreeView](../a-z/treeview.md) is checked. The result of the
method will have the 13th bit set if the item is checked.
```apl
      STATE←Form.ListView.GetItemState 11
      13⊃⌽(32⍴2)⊤STATE
1
```



The picture below illustrates the effect on the appearance of a [ListView](../a-z/listview.md) object, of setting CheckBoxes to 1.


![lv_cb](../img/lv-cb.gif)



