




<h1 class="heading"><span class="name">Mask</span></h1>
| Applies To: | [Cursor](../a-z/cursor.md) | [Icon](../a-z/icon.md) |
| --- | --- | ---  |

| Applies To: | [Cursor](../a-z/cursor.md) [Icon](../a-z/icon.md) | [Cursor](../a-z/cursor.md) | [Icon](../a-z/icon.md) |  |
| --- | --- | ---  |
| [Cursor](../a-z/cursor.md) | [Icon](../a-z/icon.md) |  |


Description


This property is used to specify how the bitmap for a [Cursor](../a-z/cursor.md) or [Icon](../a-z/icon.md) interacts with the pixels of the screen when it is displayed.


When a [Cursor](../a-z/cursor.md) or [Icon](../a-z/icon.md) is displayed, the colour of each pixel occupied by the object on the screen is determined by :

- The colour specified by [Bits](../a-z/bits.md) via [CMap](../a-z/cmap.md)
- The value of Mask
- The existing colour of the screen pixel

Mask is a Boolean matrix with the same shape as the [Bits](../a-z/bits.md) property. See [Cursor](../a-z/cursor.md) and [Icon](../a-z/icon.md) objects for further details.



