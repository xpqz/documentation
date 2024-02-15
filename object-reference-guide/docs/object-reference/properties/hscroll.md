




<h1 class="heading"><span class="name">HScroll</span></h1>

**Applies To**


**Description**


For most objects to which it applies, this property determines whether or not a horizontal scrollbar is provided.



**HScroll may only be set when the object is created with ⎕WC and may not subsequently be changed with ⎕WS or assignment.**


When applied to a [Combo](../a-z/combo.md), or to an [Edit](../a-z/edit.md) object with [Style ](../a-z/style.md)`'Single'` (i.e. a single-line edit field), the value 0 inhibits scrolling, and prevents the user from entering more data when the field is full. If instead it has the value `¯2`, the field is scrollable, and the length of data that may be entered is not limited by the length of the field.


When applied to an [Edit](../a-z/edit.md) object with [Style ](../a-z/style.md)`'Multi'` (i.e. a multi-line text box), the value 0 inhibits scrolling, and causes individual lines to be "word-wrapped". The values `¯2` and `¯1` enable sideways scrolling, and permit individual lines to exceed the width of the object. The value `¯1` means that a horizontal scrollbar is provided.


For a [Scroll](../a-z/scroll.md) object, the scrollbar is horizontal if HScroll is `¯1` and vertical if HScroll is 0. For a [Form](../a-z/form.md), a horizontal scrollbar is provided if HScroll is set to `¯1`. The default value is 0 (no scrollbar).


For a [StatusBar](../a-z/statusbar.md), [TabBar](../a-z/tabbar.md) or [ToolBar](../a-z/toolbar.md) with [Align](../a-z/align.md) set to Top or Bottom, HScroll determines whether or not a horizontal scrollbar is provided and how the object positions its children. If HScroll is 0 (the default) the object organises its children in multiple rows and does not provide a scrollbar. If HScroll is `¯1` or `¯2`, the object organises its children in a single row and provides a mini scrollbar to allow those positioned beyond the right edge of the object to be scrolled into view. If HScroll is `¯1`, the scrollbar is always shown. If HScroll is `¯2`, it is only shown when needed.


For a [Grid](../a-z/grid.md), HScroll may be `0` (no horizontal scrollbar), `¯1` (scrollbar is displayed when required), `¯2` (same as `¯1`) or `¯3` (scrollbar is always displayed).


