




<h1 class="heading"><span class="name">Mask</span></h1>

Applies To: [Cursor](./cursor.md) [Icon](./icon.md)


**Description**


This property is used to specify how the bitmap for a [Cursor](./cursor.md) or [Icon](./icon.md) interacts with the pixels of the screen when it is displayed.


When a [Cursor](./cursor.md) or [Icon](./icon.md) is displayed, the colour of each pixel occupied by the object on the screen is determined by :

- The colour specified by [Bits](bits.md) via [CMap](cmap.md)
- The value of Mask
- The existing colour of the screen pixel

Mask is a Boolean matrix with the same shape as the [Bits](bits.md) property. See [Cursor](./cursor.md) and [Icon](./icon.md) objects for further details.



