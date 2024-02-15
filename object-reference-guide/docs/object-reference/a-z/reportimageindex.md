




<h1 class="heading"><span class="name">ReportImageIndex</span></h1>
| Applies To: | [ListView](./listview.md) |
| --- | ---  |

| Applies To: | [ListView](./listview.md) | [ListView](./listview.md) |  |  |
| --- | --- | ---  |
| [ListView](./listview.md) |  |  |


Description


The ReportImageIndex property is an integer scalar or matrix  that specifies the images to be displayed alongside each item  in a [ListView](./listview.md) object in Report View.


If it is a matrix, its first column specifies the indices of the icons to be displayed against the [Items](items.md) of the [ListView](./listview.md), overriding the icons specified by [ImageIndex](imageindex.md), and its subsequent columns specify the indices of the icons to be displayed against the elements of [ReportInfo](reportinfo.md).


i.e. if non-scalar, `(⍴ReportImageIndex)←→(0 1+⍴ReportInfo)`


Each  element of ReportImageIndex specifies an index into the [ImageList](./imagelist.md) object specified by the [ImageListObj](imagelistobj.md) property.



