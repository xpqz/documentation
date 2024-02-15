




<h1 class="heading"><span class="name">Justify</span></h1>

| Applies To: | [Button](../a-z/button.md) | [ButtonEdit](../a-z/buttonedit.md) | [Edit](../a-z/edit.md) | [Label](../a-z/label.md) | [Spinner](../a-z/spinner.md) | [TabControl](../a-z/tabcontrol.md) |
| --- | --- | --- | --- | --- | --- | ---  |


**Description**


This property determines the manner in which text is justified within the object. It is a character vector that may take the value `'Left'` (the default), `'Centre'` or `'Right'`. The keyword `'Centre'` may also be spelled `'Center'`.


When applied to an [Edit](../a-z/edit.md) object with [Style](../a-z/style.md) `'Multi'`, a value of `'Centre'` or `'Right'` forces word-wrapping and disables horizontal scrolling. Note that Justify only applies to a multi-line edit field. If you specify a value for Justify in a 1-line edit field ([Style](../a-z/style.md) `'Single'`), it will be ignored.


For a [TabControl](../a-z/tabcontrol.md), Justify may be `'Right'` (which is the default) or `'None'` or empty.


If Justify is `'Right'`, the [TabControl](../a-z/tabcontrol.md) increases the width of each tab, if necessary, so that each row of tabs fills the entire width of the tab control. Otherwise, if Justify is empty or 'None', the rows are ragged.


With the exception of [Label](../a-z/label.md) and [TabControl](../a-z/tabcontrol.md) objects, Justify may only be specified when the object is created using `⎕WC`.



