




<h1 class="heading"><span class="name">ComboEx</span></h1>

| [Parents](../ParentLists/ComboEx.htm) | [Children](../ChildLists/ComboEx.htm) | [Properties](../PropLists/ComboEx.htm) | [Methods](../MethodLists/ComboEx.htm) | [Events](../EventLists/ComboEx.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | The ComboEx object is an extended version of the Combo object that provides additional features including item images |
| --- | ---  |


**Description**


The ComboEx object is a ComboBox that supports item images and indenting. It is a superset of the [Combo](../a-z/combo.md) object and supports all its functionality. For further details, see ["Combo" on page 1](../a-z/combo.md).



For most purposes, you can use the ComboEx object in place of the [Combo](../a-z/combo.md) object whether or not you make use of the extended features of the ComboEx.


Like the basic [Combo](../a-z/combo.md), the list of text items in the ComboEx is specified by the [Items](../a-z/items.md) property. You may associate images with each of the text items using the [ImageListObj](../a-z/imagelistobj.md), [ImageIndex](../a-z/imageindex.md) and [SelImageIndex](../a-z/selimageindex.md) properties.


To do so, [ImageListObj](../a-z/imagelistobj.md) specifies the name of an ImageList object that contains a set of images. [ImageIndex](../a-z/imageindex.md) and [SelImageIndex](../a-z/selimageindex.md) map individual images from the ImageList to each of the text items specified by Items. [ImageIndex](../a-z/imageindex.md) specifies the image to be displayed when the item is not selected; [SelImageIndex](../a-z/selimageindex.md) specifies the image to be displayed when the item is selected.


The [Indents](../a-z/indents.md) property specifies the amount by which each of the items are indented in units of 10 pixels


The appearance of the items is additionally controlled by the [EditImage](../a-z/editimage.md) and [EditImageIndent](../a-z/editimageindent.md) properties. These are Boolean and their effect is summarised in the table below. Notice that Images are displayed only if both these properties are set to 1 (which is the default).


There are certain restrictions that apply to a ComboEx object with Style `'Simple'`, namely:

- images and indents do not apply to the edit control portion of the object.
- the object may not redraw properly if [EditImage](../a-z/editimage.md) and/or [EditImageIndent](../a-z/editimageindent.md) are set to 0 or if [CaseSensitive](../a-z/casesensitive.md) or [PathWordBreak](../a-z/pathwordbreak.md) are set to 1.
- [PathWordBreak](../a-z/pathwordbreak.md) does not work.

|  | EditImageIndent | EditImageIndent |
| --- | --- | ---  |
| EditImage | 0 | 1 |
| 0 | No images displayed, item text is indented as specified by [Indents](../a-z/indents.md) | No images displayed, item text is indented as specified by [Indents](../a-z/indents.md) plus the width of the images in ImageList |
| 1 | No images displayed, item text is indented as specified by [Indents](../a-z/indents.md) | Images are displayed, items are indented as specified by [Indents](../a-z/indents.md) |



