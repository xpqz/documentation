




<h1 class="heading"><span class="name">ItemGroupMetrics</span></h1>

Applies To: [ListView](../a-z/listview.md)


**Description**


This property is used to specify colours and spacing elements for a [ListView](../a-z/listview.md) that is displaying its Items in groupings (see [ItemGroups](../a-z/itemgroups.md)).


ItemGroupMetrics is a 3-item nested vector as follows:


| `[1]` | Text Colours | 2-element vector of 3 element RGB values that specifies the colour of        the group caption and group footer respectively. |
| --- | --- | ---  |
| `[2]` | Spacing | 4-element integer vector that specifies the top, left, bottom and        right spacing around each grouping in pixels |
| `[3]` | Border | Colours4-element vector of 3 element RGB values that specifies the        colours for the top, left, bottom and right borders (not yet      implemented). |


The following expression, coupled with the code shown in the SetGroups example, causes the items to be displayed as shown below.
```apl
      F.L.ItemGroupMetrics[1 2]←(2⍴⊂255 0 0)(10 100 0 10)
```


![lvsg2](../img/lvsg2.gif)



**Note that this feature only applies if Native Look and Feel (see page 1) is enabled.**


