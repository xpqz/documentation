




<h1 class="heading"><span class="name">Masked</span></h1>
| Applies To: | [ImageList](../a-z/imagelist.md) |
| --- | ---  |

| Applies To: | [ImageList](../a-z/imagelist.md) | [ImageList](../a-z/imagelist.md) |  |  |
| --- | --- | ---  |
| [ImageList](../a-z/imagelist.md) |  |  |


Description


The Masked property specifies whether or not the [ImageList](../a-z/imagelist.md) will contain opaque or transparent images. It may be 0, 1(the default), 2, or 3.



Masked must be established when the [ImageList](../a-z/imagelist.md) is created by `⎕WC` and may not subsequently be altered. An inappropriate value of Masked will cause the images to be drawn incorrectly.


If Masked is 0, the [ImageList](../a-z/imagelist.md) expects opaque [Bitmap](../a-z/bitmap.md) objects.


If Masked is 1, the [ImageList](../a-z/imagelist.md) expects low-colour (4-bit or 8-bit) [Icon](../a-z/icon.md) objects whose transparency is defined by their [Mask](../a-z/mask.md) property.


If Masked is 2,  the [ImageList](../a-z/imagelist.md) expects [Bitmap](../a-z/bitmap.md) or [Icon](../a-z/icon.md) objects whose alpha channel (the degree of transparency of each pixel) is encoded in its source file along with the colours.


If Masked is 3 and Native Look and Feel 
(see page 1)
 is enabled, the behaviour is the same as if Masked were 2. If Native Look and Feel is not enabled, it behaves as if Masked were 1. This setting provides the greatest degree of portability for applications whose users may or may not have Native Look and Feel enabled. This value is used for the ImageLists on the Dyalog Session CoolBars.


