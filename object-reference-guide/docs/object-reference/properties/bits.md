




<h1 class="heading"><span class="name">Bits</span></h1>
| Applies To: | [Bitmap](../a-z/bitmap.md) | [Clipboard](../a-z/clipboard.md) | [Cursor](../a-z/cursor.md) | [Icon](../a-z/icon.md) |
| --- | --- | --- | --- | ---  |

| Applies To: | [Bitmap](../a-z/bitmap.md) [Clipboard](../a-z/clipboard.md) [Cursor](../a-z/cursor.md) [Icon](../a-z/icon.md) | [Bitmap](../a-z/bitmap.md) | [Clipboard](../a-z/clipboard.md) | [Cursor](../a-z/cursor.md) | [Icon](../a-z/icon.md) |  |  |
| --- | --- | ---  |
| [Bitmap](../a-z/bitmap.md) | [Clipboard](../a-z/clipboard.md) | [Cursor](../a-z/cursor.md) |
| [Icon](../a-z/icon.md) |  |  |


Description


This property defines the pattern in a [Bitmap](../a-z/bitmap.md), [Cursor](../a-z/cursor.md), or [Icon](../a-z/icon.md) object, or the pattern of a bitmap stored in the Windows clipboard.


For a [Bitmap](../a-z/bitmap.md), [Clipboard](../a-z/clipboard.md) or [Icon](../a-z/icon.md), Bits is an integer matrix each of whose elements represents the colour of the corresponding pixel in the bitmap. The colours are specified as 0-origin indices into the [CMap](../a-z/cmap.md) property, which itself defines the complete set of different colours (the colour map) used by the object.


Please note that Bits and [CMap](../a-z/cmap.md) may only be used to represent an image with a colour palette of 256 colours or less. If the colour palette is larger, the values of Bits and [CMap](../a-z/cmap.md) reported by `⎕WG` will be (0 0). For a high-colour image, use [CBits](../a-z/cbits.md) instead.


For a [Cursor](../a-z/cursor.md), Bits is a Boolean matrix which specifies the shape of the cursor. For a [Cursor](../a-z/cursor.md) and [Icon](../a-z/icon.md), Bits is used in conjunction with the [Mask](../a-z/mask.md) property.


See [CMap](../a-z/cmap.md) for further details.



