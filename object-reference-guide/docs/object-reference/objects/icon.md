




<h1 class="heading"><span class="name">Icon</span></h1>

[Parents](../ParentLists/Icon.htm) [Children](../ChildLists/Icon.htm) [Properties](../PropLists/Icon.htm) [Methods](../MethodLists/Icon.htm) [Events](../EventLists/Icon.htm)


Purpose: This object defines an icon.


**Description**


The [File](../a-z/file.md) property specifies the name of an icon  file (.ICO. .GIF or .PNG), or the name of a DLL or EXE file and the identity of the icon within it.



The Style property identifies the size of the icon and must be `'Large'` or `'Small'`. The former specifies a 32x32 icon and is the default; the latter specifies a 16x16 icon. The size of the icon is not embedded within the icon data, so it is **essential** to specify Style correctly. Note that a single file may contain both sizes of an icon. Style is only relevant when loading an Icon from file.


If the value of the [File](../a-z/file.md) property is set by [`⎕WS`](../../Language/System Functions/ws.htm), no immediate action is taken, but the corresponding file may subsequently be read or written using the [FileRead](../a-z/fileread.md) or [FileWrite](../a-z/filewrite.md) methods.


16-bit icons contain fewer than 256 colours and each pixel is either transparent or opaque. The images in such Icons are represented by the [Bits](../a-z/bits.md), [Mask](../a-z/mask.md) and [CMap](../a-z/cmap.md) properties.


32-bit icons are 24-bit images with an 8-bit alpha channel which specifies the degree of transparency of each pixel. The pixels in these Icons are represented by the [CBits](../a-z/cbits.md) property.


[CBits](../a-z/cbits.md) is a rank-2 numeric array whose dimensions represent the rows and columns of pixels in the Icon. The values in [CBits](../a-z/cbits.md) represent the colour and of each pixel and also its transparency.


[Bits](../a-z/bits.md) is an integer matrix whose elements define the colours of each pixel in the icon in terms of their (0-origin) indices into [CMap](../a-z/cmap.md). When the icon is displayed on the screen, the way in which these colours combine with those currently displayed on the screen (the background) is specified by [Mask](../a-z/mask.md). This is a Boolean matrix of the same size as [Bits](../a-z/bits.md). The following table shows how the colour of each resulting pixel is determined.


| Bits | Colour | 0 | Colour |
| --- | --- | --- | ---  |
| Mask | 0 | 1 | 1 |
| Pixel | Colour | Background | New Colour |


If an element of [Mask](../a-z/mask.md) is 0, the corresponding element of [Bits](../a-z/bits.md) defines the colour of the resulting pixel that is displayed on the screen. If an element of [Mask](../a-z/mask.md) is 1, the resulting pixel that is displayed on the screen is either the current background colour or is a new colour chosen by MS-Windows to be visible against the background. A non rectangular icon is obtained by setting those elements of [Bits](../a-z/bits.md) and [Mask](../a-z/mask.md) that you want to exclude from the shape to be 0 and 1 respectively.


The size of [Bits](../a-z/bits.md) is restricted by the capabilities of the current display driver. [Mask](../a-z/mask.md) must have the same shape as [Bits](../a-z/bits.md).


An Icon is **used** by setting the [IconObj](../a-z/iconobj.md) property or [Picture](../a-z/picture.md) property of another object to its name or ref.


