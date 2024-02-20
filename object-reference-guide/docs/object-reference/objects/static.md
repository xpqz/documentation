




<h1 class="heading"><span class="name">Static</span></h1>

[Parents](../ParentLists/Static.htm) [Children](../ChildLists/Static.htm) [Properties](../PropLists/Static.htm) [Methods](../MethodLists/Static.htm) [Events](../EventLists/Static.htm)


Purpose: This object is primarily used to display graphics in a sub-window.


**Description**


The overall appearance of an empty Static object is controlled by the value of its [Style](../a-z/style.md) property which may be one of the following character vectors:



Note that the colours implied by the [Style](../a-z/style.md) are not "hard-coded" but are actually defined by the current Windows colour scheme as follows:


| Black | Window Border Colour |
| --- | ---  |
| Grey/Gray | Desktop Colour |
| White | Window Background Colour |


If the background colour of the [Form](../a-z/form.md) is also set to the Window Background Colour, it follows that the [Style](../a-z/style.md)s `'WhiteFrame'` and `'WhiteBox'` make the Static itself invisible (against the background), although the **contents** of the Static will show. This makes the Static appear like an invisible clipping window.


| `'BlackFrame'` | `'BlackBox'` |
| --- | ---  |
| `'GreyFrame' or 'GrayFrame'` | `'GreyBox' or 'GrayBox'` |
| `'WhiteFrame'` | `'WhiteBox'` |


