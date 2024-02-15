




<h1 class="heading"><span class="name">View</span></h1>
| Applies To: | [ListView](../a-z/listview.md) |
| --- | ---  |

| Applies To: | [ListView](../a-z/listview.md) | [ListView](../a-z/listview.md) |  |  |
| --- | --- | ---  |
| [ListView](../a-z/listview.md) |  |  |


Description


The View property specifies how the items in a [ListView](../a-z/listview.md) object are displayed. It is a character vector which may have one of the following values; `'Icon'` (the default), `'SmallIcon'`, `'List'` or `'Report'`.



When View is `'Icon'` or `'SmallIcon'`, the items are arranged *row-wise* with large or small icons as appropriate. When View is set to `'List'`, the items are arranged *column-wise* using small icons. When View is set to `'Report'`, the items are displayed in a single column using small icons but with the matrix specified by [ReportInfo](../a-z/reportinfo.md) displayed alongside. In this format, the ListView also provides column headings which are specified by the ColTitles property. The alignment of these titles (and of the data in the columns beneath them) is defined by the [ColTitleAlign](../a-z/coltitlealign.md) property. Examples of different views are illustrated below.


![listview_icon](../img/listview-icon.png)


![listview_list](../img/listview-list.png)


![listview_report](../img/listview-report.png)


