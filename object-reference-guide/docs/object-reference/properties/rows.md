




<h1 class="heading"><span class="name">Rows</span></h1>
| Applies To: | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) |
| --- | --- | ---  |

| Applies To: | [Combo](../a-z/combo.md) [ComboEx](../a-z/comboex.md) | [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) |  |
| --- | --- | ---  |
| [Combo](../a-z/combo.md) | [ComboEx](../a-z/comboex.md) |  |


Description


For [Combo](../a-z/combo.md) objects with [Style](../a-z/style.md)`'Drop'` or `'DropEdit'` this property determines the number of rows displayed in the drop-down listbox when it is displayed. Note that the height of the edit field of a [Combo](../a-z/combo.md) of this type is dependent only upon the size of the font in use, and cannot otherwise be changed.


Rows is a "read-only" property for a [Combo](../a-z/combo.md) with [Style ](../a-z/style.md)`'Simple'` and an attempt to set it in a [Combo](../a-z/combo.md) of this type with `⎕WC` or `⎕WS` will generate a `NONCE ERROR`. Instead, the overall height of a Simple [Combo](../a-z/combo.md) is determined by the first element of the [Size](../a-z/size.md) property.



