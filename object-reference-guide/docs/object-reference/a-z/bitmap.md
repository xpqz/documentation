




<h1 class="heading"><span class="name">Bitmap</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | A graphical object used to represent a bitmap which may be used both to display a picture or as a pattern (brush) used to fill other objects. |
| --- | --- | ---  |
| Parents | [Detach](./detach.md) [FileRead](./fileread.md) [FileWrite](./filewrite.md) [MakePNG](./makepng.md) [MakeGIF](./makegif.md) [GetTextSize](./gettextsize.md) | [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) | [MakePNG](./makepng.md) | [MakeGIF](./makegif.md) | [GetTextSize](./gettextsize.md) |
| [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) |
| [MakePNG](./makepng.md) | [MakeGIF](./makegif.md) | [GetTextSize](./gettextsize.md) |
| Children | [Detach](./detach.md) [FileRead](./fileread.md) [FileWrite](./filewrite.md) [MakePNG](./makepng.md) [MakeGIF](./makegif.md) [GetTextSize](./gettextsize.md) | [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) | [MakePNG](./makepng.md) | [MakeGIF](./makegif.md) | [GetTextSize](./gettextsize.md) |
| [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) |
| [MakePNG](./makepng.md) | [MakeGIF](./makegif.md) | [GetTextSize](./gettextsize.md) |
| Properties | [Detach](./detach.md) [FileRead](./fileread.md) [FileWrite](./filewrite.md) [MakePNG](./makepng.md) [MakeGIF](./makegif.md) [GetTextSize](./gettextsize.md) | [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) | [MakePNG](./makepng.md) | [MakeGIF](./makegif.md) | [GetTextSize](./gettextsize.md) |
| [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) |
| [MakePNG](./makepng.md) | [MakeGIF](./makegif.md) | [GetTextSize](./gettextsize.md) |
| Methods | [Detach](./detach.md) [FileRead](./fileread.md) [FileWrite](./filewrite.md) [MakePNG](./makepng.md) [MakeGIF](./makegif.md) [GetTextSize](./gettextsize.md) | [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) | [MakePNG](./makepng.md) | [MakeGIF](./makegif.md) | [GetTextSize](./gettextsize.md) |
| [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) |
| [MakePNG](./makepng.md) | [MakeGIF](./makegif.md) | [GetTextSize](./gettextsize.md) |
| Events | [Detach](./detach.md) [FileRead](./fileread.md) [FileWrite](./filewrite.md) [MakePNG](./makepng.md) [MakeGIF](./makegif.md) [GetTextSize](./gettextsize.md) | [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) | [MakePNG](./makepng.md) | [MakeGIF](./makegif.md) | [GetTextSize](./gettextsize.md) |
| [Detach](./detach.md) | [FileRead](./fileread.md) | [FileWrite](./filewrite.md) |
| [MakePNG](./makepng.md) | [MakeGIF](./makegif.md) | [GetTextSize](./gettextsize.md) |


Description


A Bitmap may be created either from a file (.BMP, .GIF or .PNG) or from APL arrays. To create a Bitmap object using `⎕WC`, you can either specify the [File](./file.md) property or the [CBits](./cbits.md) property, or the [Bits](./bits.md) and [CMap](./cmap.md) properties.



If you specify [File](./file.md), it should contain the name of a bitmap file from which the bitmap is to be read. If omitted, a .BMP file extension is added. You may also load a Bitmap from a DLL or from the DYALOG.EXE executable. See [File](./file.md) property for details.


If instead you want to create a Bitmap dynamically from APL variables, you may do so in one of two ways.


For a palette of up to 256 colours, you may specify the image using the [Bits](./bits.md) and [CMap](./cmap.md) properties. The alternative is to use the [CBits](./cbits.md) property which works for any size of colour palette.


If [MaskCol](./maskcol.md) is non-zero, it specifies the transparent colour for the Bitmap. Any pixels specified with the same colour will instead be displayed in whatever colour is underneath the Bitmap. This achieves similar behaviour to that of an Icon.


The [KeepBits](./keepbits.md) property has the value 0 or 1, and controls how a Bitmap is saved in the workspace. A value of 0 (the default) means that the values of [CBits](./cbits.md), [Bits](./bits.md) and [CMap](./cmap.md) are not kept in the workspace. If you request the values of [CBits](./cbits.md), [Bits](./bits.md) or [CMap](./cmap.md) with `⎕WG`, they are obtained directly from the corresponding Windows bitmap resource. When the workspace is `)LOAD`ed, the Bitmap is recreated from the associated file defined by the value of the [File](./file.md) property. Note that if this file doesn't exist when the workspace is `)LOAD`ed, the Bitmap is not created, but no error is generated. However, when you reference the object you will get a `VALUE ERROR`.


If [KeepBits](./keepbits.md) is 1, the values of [CBits](./cbits.md), [Bits](./bits.md) and [CMap](./cmap.md) are stored permanently in the workspace, and are used to rebuild the Bitmap when the workspace is `)LOAD`ed. In this case, the file name (if any) is ignored. Setting [KeepBits](./keepbits.md) to 1 uses more workspace, but may be more convenient if you want to distribute applications.


The [Size](./size.md) property allows you to query the size of a Bitmap without having to retrieve the [CBits](./cbits.md) or [Bits](./bits.md) property and then take its "shape". This will be noticeably faster for a large Bitmap. If you set the [Size](./size.md) property using `⎕WS` the Bitmap is scaled to the new size.


A useful feature of a Bitmap is that it can be the parent of any of the graphical objects. This allows you to create or edit a bitmap by drawing lines, circles, etc. in it.


The [FileRead](./fileread.md) (90) and [FileWrite](./filewrite.md) (91) methods allow you to dynamically manage bitmap files (.BMP). The expression:
```apl
      bmname.FileWrite
```


causes the Bitmap called `bmname` to be written to the file specified by the current value of the [File](./file.md) property. The file is automatically written in standard bitmap format. Similarly, the expression:
```apl
      bmname.FileRead
```


causes the Bitmap called `bmname` to be redefined from the bitmap file specified by the current value of the [File](./file.md) property.


The [MakeGIF](./makegif.md) and [MakePNG](./makepng.md) methods may be used to convert the image represented by a Bitmap object into a GIF or PNG data stream, suitable for display in a web browser. The [TCPSendPicture](./tcpsendpicture.md) method may be used to transfer a Bitmap on a TCP/IP socket.


Using a bitmap is always a 2-stage process. First you create a Bitmap object with `⎕WC`. Then you use it by specifying its name as a property of another object.


The [Picture](./picture.md) property specifies the name of a Bitmap to be displayed in an [ActiveXControl](activexcontrol.md), [Button](button.md), Form, [Group](group.md), [Image](image.md), MDIClient, Sm, [Static](static.md), StatusBar, [StatusField](statusfield.md), [SubForm](subform.md), TabBar, or [ToolBar](toolbar.md).


The [BtnPix](./btnpix.md) property specifies three Bitmaps to be used to represent the 3 states of a [Button](button.md), Menu or MenuItem.


The [FStyle](./fstyle.md) property specifies the name of a Bitmap to be used as a pattern to fill a Poly, [Ellipse](ellipse.md) or [Rect](rect.md) object.


