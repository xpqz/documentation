




<h1 class="heading"><span class="name">ColTitleAlign</span></h1>

Applies To: [Grid](./grid.md) [ListView](./listview.md)


**Description**


The ColTitleAlign property specifies the alignment of column titles. For a [ListView](./listview.md) object this is only relevant only when the [View](view.md) property is set to `'Report'`. ColTitleAlign is either a simple character vector, or a vector of character vectors with one element per column.


For a [Grid](./grid.md), ColTitleAlign may be:'Top', `'Bottom'`, `'Left'`, `'Right'`, `'Centre'`, `'TopLeft'`, `'TopRight'`, `'BottomLeft'`, or `'BottomRight'`.


For a [ListView](./listview.md) object, ColTitleAlign may be`'Left'`, `'Right'` or `'Centre'`. Also, for a [ListView](./listview.md) the column data itself is aligned likewise. Note that the *first* column in a [ListView](./listview.md) is always left-aligned regardless of the setting of ColTitleAlign. This is a Windows restriction.


Note that both spellings `'Centre'` and `'Center'` are accepted.



