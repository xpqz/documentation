




<h1 class="heading"><span class="name">VScroll</span></h1>

**Applies To**


**Description**


This property determines whether or not an object has a vertical scrollbar. It is a single integer with the value `¯2`, `¯1`, or 0.



**VScroll may only be set when the object is created with ⎕WC and may not subsequently be changed with ⎕WS or assignment.**


For a [Form](../a-z/form.md) object, the value `¯1`  specifies that the [Form](../a-z/form.md) has a vertical scrollbar. A value of 0 (which is the default) means that it does not.


When applied to an [Edit](../a-z/edit.md) object, the value `¯2` specifies that the data is scrollable vertically, but only by using the cursor keys; a scrollbar is not provided. A value of `¯1` causes a scrollbar to be displayed (whether or not one is needed).


When applied to a [List](../a-z/list.md) object, the value `¯2` specifies that the data is scrollable vertically, but only by using the cursor keys; a scrollbar is not provided. A value of `¯1` causes a scrollbar to be displayed if required (when the list of items exceeds the height of the object).


When applied to a [Combo](../a-z/combo.md) or [ComboEx](../a-z/comboex.md) object, a value of `¯1` or `¯2` causes a scrollbar to be displayed, whether or not one is required.


For all these objects, a value of 0 inhibits scrolling altogether.


For a [Scroll](../a-z/scroll.md) object, VScroll may be `¯1` or 0. If it is `¯1` the direction of the scrollbar is vertical. If both [HScroll](../a-z/hscroll.md) and VScroll are set to `¯1`, [HScroll](../a-z/hscroll.md) takes precedence and forces VScroll back to 0.


For a [StatusBar](../a-z/statusbar.md), [TabBar](../a-z/tabbar.md) or [ToolBar](../a-z/toolbar.md) with [Align](../a-z/align.md) set to Left or Right, VScroll determines whether or not a vertical scrollbar is provided and how the object positions its children. If VScroll is 0 (the default) the object organises its children in multiple columns and does not provide a scrollbar. If VScroll is `¯1` or `¯2`, the object organises its children in a single column and provides a mini scrollbar to allow those positioned beyond the bottom edge of the object to be scrolled into view. If VScroll is `¯1`, the scrollbar is always shown. If VScroll is `¯2`, it is only shown when needed.


For a [Grid](../a-z/grid.md), VScroll may be 0 (no vertical scrollbar), `¯1` (scrollbar is displayed when required), `¯2` (same as `¯1`) or `¯3` (scrollbar is always displayed).


