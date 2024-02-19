




<h1 class="heading"><span class="name">Bits</span></h1>

| Applies To: | [Bitmap](./bitmap.md) | [Clipboard](./clipboard.md) | [Cursor](./cursor.md) | [Icon](./icon.md) |
| --- | --- | --- | --- | ---  |


**Description**


This property defines the pattern in a [Bitmap](./bitmap.md), [Cursor](./cursor.md), or [Icon](./icon.md) object, or the pattern of a bitmap stored in the Windows clipboard.


For a [Bitmap](./bitmap.md), [Clipboard](./clipboard.md) or [Icon](./icon.md), Bits is an integer matrix each of whose elements represents the colour of the corresponding pixel in the bitmap. The colours are specified as 0-origin indices into the [CMap](CMap.htm) property, which itself defines the complete set of different colours (the colour map) used by the object.


Please note that Bits and [CMap](CMap.htm) may **only** be used to represent an image with a colour palette of **256 colours or less**. If the colour palette is larger, the values of Bits and [CMap](CMap.htm) reported by `⎕WG` will be (0 0). For a high-colour image, use [CBits](CBits.htm) instead.


For a [Cursor](./cursor.md), Bits is a Boolean matrix which specifies the shape of the cursor. For a [Cursor](./cursor.md) and [Icon](./icon.md), Bits is used in conjunction with the [Mask](Mask.htm) property.


See [CMap](CMap.htm) for further details.



