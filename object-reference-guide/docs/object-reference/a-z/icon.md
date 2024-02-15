




<h1 class="heading"><span class="name">Icon</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | This object defines an icon. |
| --- | --- | ---  |
| Parents | [Detach](./detach.md) [FileRead](./fileread.md) [FileWrite](./filewrite.md) | [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) |
| [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) |
| Children | [Detach](./detach.md) [FileRead](./fileread.md) [FileWrite](./filewrite.md) | [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) |
| [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) |
| Properties | [Detach](./detach.md) [FileRead](./fileread.md) [FileWrite](./filewrite.md) | [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) |
| [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) |
| Methods | [Detach](./detach.md) [FileRead](./fileread.md) [FileWrite](./filewrite.md) | [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) |
| [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) |
| Events | [Detach](./detach.md) [FileRead](./fileread.md) [FileWrite](./filewrite.md) | [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) |
| [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) |


Description


The [File](./file.md) property specifies the name of an icon  file (.ICO. .GIF or .PNG), or the name of a DLL or EXE file and the identity of the icon within it.



The Style property identifies the size of the icon and must be `'Large'` or `'Small'`. The former specifies a 32x32 icon and is the default; the latter specifies a 16x16 icon. The size of the icon is not embedded within the icon data, so it is essential to specify Style correctly. Note that a single file may contain both sizes of an icon. Style is only relevant when loading an Icon from file.


If the value of the [File](./file.md) property is set by `⎕WS`, no immediate action is taken, but the corresponding file may subsequently be read or written using the [FileRead](./fileread.md) or [FileWrite](./filewrite.md) methods.


16-bit icons contain fewer than 256 colours and each pixel is either transparent or opaque. The images in such Icons are represented by the [Bits](./bits.md), [Mask](./mask.md) and [CMap](./cmap.md) properties.


32-bit icons are 24-bit images with an 8-bit alpha channel which specifies the degree of transparency of each pixel. The pixels in these Icons are represented by the [CBits](./cbits.md) property.


[CBits](./cbits.md) is a rank-2 numeric array whose dimensions represent the rows and columns of pixels in the Icon. The values in [CBits](./cbits.md) represent the colour and of each pixel and also its transparency.


[Bits](./bits.md) is an integer matrix whose elements define the colours of each pixel in the icon in terms of their (0-origin) indices into [CMap](./cmap.md). When the icon is displayed on the screen, the way in which these colours combine with those currently displayed on the screen (the background) is specified by [Mask](./mask.md). This is a Boolean matrix of the same size as [Bits](./bits.md). The following table shows how the colour of each resulting pixel is determined.

| Bits | Colour | 0 | Colour |
| --- | --- | --- | ---  |
| Mask | 0 | 1 | 1 |
| Pixel | Colour | Background | New Colour |


If an element of [Mask](./mask.md) is 0, the corresponding element of [Bits](./bits.md) defines the colour of the resulting pixel that is displayed on the screen. If an element of [Mask](./mask.md) is 1, the resulting pixel that is displayed on the screen is either the current background colour or is a new colour chosen by MS-Windows to be visible against the background. A non rectangular icon is obtained by setting those elements of [Bits](./bits.md) and [Mask](./mask.md) that you want to exclude from the shape to be 0 and 1 respectively.


The size of [Bits](./bits.md) is restricted by the capabilities of the current display driver. [Mask](./mask.md) must have the same shape as [Bits](./bits.md).


An Icon is used by setting the [IconObj](./iconobj.md) property or [Picture](./picture.md) property of another object to its name or ref.


