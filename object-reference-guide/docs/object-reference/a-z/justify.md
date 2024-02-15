




<h1 class="heading"><span class="name">Justify</span></h1>

| Applies To: | [Button](./button.md) | [ButtonEdit](./buttonedit.md) | [Edit](./edit.md) | [Label](./label.md) | [Spinner](./spinner.md) | [TabControl](./tabcontrol.md) |
| --- | --- | --- | --- | --- | --- | ---  |


**Description**


This property determines the manner in which text is justified within the object. It is a character vector that may take the value `'Left'` (the default), `'Centre'` or `'Right'`. The keyword `'Centre'` may also be spelled `'Center'`.


When applied to an [Edit](./edit.md) object with [Style](style.md) `'Multi'`, a value of `'Centre'` or `'Right'` forces word-wrapping and disables horizontal scrolling. Note that Justify only applies to a multi-line edit field. If you specify a value for Justify in a 1-line edit field ([Style](style.md) `'Single'`), it will be ignored.


For a [TabControl](./tabcontrol.md), Justify may be `'Right'` (which is the default) or `'None'` or empty.


If Justify is `'Right'`, the [TabControl](./tabcontrol.md) increases the width of each tab, if necessary, so that each row of tabs fills the entire width of the tab control. Otherwise, if Justify is empty or 'None', the rows are ragged.


With the exception of [Label](./label.md) and [TabControl](./tabcontrol.md) objects, Justify may only be specified when the object is created using `⎕WC`.



