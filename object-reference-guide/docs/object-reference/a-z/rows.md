




<h1 class="heading"><span class="name">Rows</span></h1>

| Applies To: | [Combo](./combo.md) | [ComboEx](./comboex.md) |
| --- | --- | ---  |


**Description**


For [Combo](./combo.md) objects with [Style](style.md)`'Drop'` or `'DropEdit'` this property determines the number of rows displayed in the drop-down listbox when it is displayed. Note that the height of the edit field of a [Combo](./combo.md) of this type is dependent only upon the size of the font in use, and cannot otherwise be changed.


Rows is a "read-only" property for a [Combo](./combo.md) with [Style ](style.md)`'Simple'` and an attempt to set it in a [Combo](./combo.md) of this type with [`⎕WC`](../../Language/System%20Functions/wc.htm) or [`⎕WS`](../../Language/System%20Functions/ws.htm) will generate a `NONCE ERROR`. Instead, the overall height of a Simple [Combo](./combo.md) is determined by the first element of the [Size](size.md) property.



