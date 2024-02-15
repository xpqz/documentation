




<h1 class="heading"><span class="name">ReportBCol</span></h1>

| Applies To: | [ListView](./listview.md) |
| --- | ---  |


**Description**


In Report View, the ReportBCol property is either a scalar or a matrix  that specifies the background colours for each item displayed in a [ListView](./listview.md) object .


Its first column refers to the [Items](items.md) themselves, and subsequent columns to the elements of [ReportInfo](reportinfo.md).


i.e. if non-scalar, `(⍴ReportBCol)←→(0 1+⍴ReportInfo)`


Each  element of ReportBCol is either an integer colour value or a 3-element of RGB colour indices.


For further information, see ["BCol" on page 1](bcol.md).



