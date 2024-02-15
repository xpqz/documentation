




<h1 class="heading"><span class="name">ListView</span></h1>

| [Parents](../ParentLists/ListView.htm) | [Children](../ChildLists/ListView.htm) | [Properties](../PropLists/ListView.htm) | [Methods](../MethodLists/ListView.htm) | [Events](../EventLists/ListView.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | The ListView object displays a collection of items. |
| --- | ---  |


**Description**


The ListView object is a window that displays a collection of items, each
item consisting of an icon and a label. The ListView provides several ways of
arranging items and displaying individual items. For example, additional
information about each item can be displayed in columns to the right of the icon
and label. An example of the use of a ListView object is the "My Computer"
Windows utility.



The Items property is a vector of character vectors that specifies the labels
for the items displayed by the ListView. The [ImageListObj](./imagelistobj.md) property specifies the names of two [ImageList](imagelist.md) objects that define two sets of icons; a large icon (32x32 pixel) set and a
small icon (16x16 pixel) set. Alternatively, [ImageListObj](./imagelistobj.md) may be empty (no icons
displayed) or contain just the name of a single large icon [ImageList](imagelist.md).


The [View](./view.md) property contains a character
vector that determines how the items are displayed. It may have one of the
following values; `'Icon'` (the default), `'SmallIcon'`,
`'List'` or `'Report'`.
When View is `'Icon'` or `'SmallIcon'`,
the items are arranged *row-wise* with large or small icons as appropriate.
When View is set to `'List'`, the items are
arranged *column-wise* using small icons. Examples of `'Icon'` and `'List'` views are illustrated below.


![listview_icon](../img/listview-icon.png)


![listview_list](../img/listview-list.png)


When View is set to `'Report'`, the items
are displayed in a single column using small icons but with the matrix specified
by [ReportInfo](./reportinfo.md) displayed alongside. In
this format, the Boolean [Header](./header.md) property
determines whether or not the object also provides column headings. Its default
value is 1. The column headings themselves are specified by the ColTitles
property. Their alignment (and the alignment of the data in the columns beneath
them) is defined by the [ColTitleAlign](./coltitlealign.md) property.


The appearance of the column titles is further controlled by the [ColTitle3D](./coltitle3d.md) property. This is a Boolean value (default 1) which specifies whether or not the
column titles have a 3-dimensional (plinth) appearance. [Header](./header.md) and [ColTitle3D](./coltitle3d.md) may only be set when the
object is created using `⎕WC` and may
not subsequently be changed by `⎕WS`.


In `'Report'` View, columns may be
resized by the user dragging the bars between the titles, or under program
control using the SetColSize event. A `'Report'` view example is illustrated below.


![listview_report](../img/listview-report.png)


The [DragItems](./dragitems.md) property is Boolean and
specifies whether or not the user may drag an item from one position to another.
Its default value is 1 (dragging is enabled).


The [AutoArrange](./autoarrange.md) property is Boolean
and specifies whether or not the items are automatically re-arranged whenever an
item is repositioned by the user or moved under program control. Its default
value is 0.


The [EditLabels](./editlabels.md) is a Boolean property
(default 0) that determines whether or not the user may edit the labels which
are specified by the Items property.


The [Style](./style.md) property may be `'Single'`,
which specifies that only one item may be selected at a time, or `'Multi'` which permits multiple selections to be made. The default is `'Multi'`.


The [CheckBoxes](./checkboxes.md) property is Boolean
and specifies whether or not check boxes are drawn to the left of items. Its
default value is 0.


The [GridLines](./gridlines.md) property is Boolean and
specifies whether or not grid lines are drawn between items. This applies only
when View is `'Report'`. Its default value
is 0.


In `'Report'` View, the [ReportImageIndex](./reportimageindex.md) property specify images to be displayed alongside each item, and overrides the images specified by [ImageListObj](./imagelistobj.md). The [HeaderImageList](./headerimagelist.md) and [HeaderImageIndex](./headerimageindex.md)  properties specify images to be displayed alongside each column title.


The following example illustrates the use of these properties.


![listview_weather](../img/listview-weather.png)


The [ReportBCol](./reportbcol.md) property specifies each item's background colour.


The [FullRowSelect](./fullrowselect.md) property is
Boolean and specifies whether or not the entire row is highlighted to indicate
selected items. This applies only when View is `'Report'`.
Its default value is 0.


The [ItemGroups](./itemgroups.md) and [ItemGroupMetrics](./itemgroupmetrics.md) properties allow you to display items in groups as illustrated below.


![lvsg1](../img/lvsg1.gif)


**Note that this feature only applies if Native Look and Feel (see page 1) is enabled.**


