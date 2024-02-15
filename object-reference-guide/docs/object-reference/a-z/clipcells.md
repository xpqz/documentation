




<h1 class="heading"><span class="name">ClipCells</span></h1>

| Applies To: | [Grid](./grid.md) |
| --- | ---  |


**Description**


This property determines whether or not the [Grid](./grid.md) displays partial cells. The default is 1. If you set ClipCells to 0, the [Grid](./grid.md) displays only complete cells and automatically fills the space between the last visible cell and the edge of the [Grid](./grid.md) with the [GridBCol](gridbcol.md) colour.


The first picture below shows a default [Grid](./grid.md) (ClipCells is 1) in which the third column of data is in fact incomplete (clipped), although this is by no means apparent to the user. The second picture shows the effect on the [Grid](./grid.md) of setting ClipCells to 0 which prevents such potential confusion.


![clip1](../img/clip1.gif)


![clip2](../img/clip2.gif)



