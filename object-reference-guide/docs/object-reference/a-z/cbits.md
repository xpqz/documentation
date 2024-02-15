



<h1 class="heading"><span class="name">CBits</span></h1>

| Applies To: | [Bitmap](./bitmap.md) | [Clipboard](./clipboard.md) | [Icon](./icon.md) |
| --- | --- | --- | ---  |


**Description**


The CBits property represents the pixels that make up a picture..


CBits provides an alternative representation to that provided by the [Bits](bits.md) and [CMap](cmap.md) properties which apply only to images with 256 colours or under. CBits may be used to represent both low-colour and high-colour images.


CBits is a rank-2 numeric array whose dimensions represent the rows and columns of pixels in the image. The values in CBits represent the colour of each pixel and (for an [Icon](./icon.md)) its transparency.


For a [Bitmap](./bitmap.md), the colour value of each pixel is obtained by encoding the red, green and blue components, i.e.
```apl
      PIXEL←256⊥RED GREEN BLUE
```


where `RED`, `GREEN` and `BLUE` are numbers in the range 0-255.


