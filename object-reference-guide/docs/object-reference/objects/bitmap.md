




<h1 class="heading"><span class="name">Bitmap</span></h1>

[Parents](../ParentLists/Bitmap.htm) [Children](../ChildLists/Bitmap.htm) [Properties](../PropLists/Bitmap.htm) [Methods](../MethodLists/Bitmap.htm) [Events](../EventLists/Bitmap.htm)


Purpose: A graphical object used to represent a bitmap which may be used both to display a picture or as a pattern (brush) used to fill other objects.


**Description**


A Bitmap may be created either from a file (.BMP, .GIF or .PNG) or from APL arrays. To create a Bitmap object using [`⎕WC`](../../Language/System Functions/wc.htm), you can either specify the [File](../a-z/file.md) property **or** the [CBits](../a-z/cbits.md) property, **or** the [Bits](../a-z/bits.md) and [CMap](../a-z/cmap.md) properties.



If you specify [File](../a-z/file.md), it should contain the name of a bitmap file from which the bitmap is to be read. If omitted, a .BMP file extension is added. You may also load a Bitmap from a DLL or from the DYALOG.EXE executable. See [File](../a-z/file.md) property for details.


If instead you want to create a Bitmap dynamically from APL variables, you may do so in one of two ways.


For a palette of up to 256 colours, you may specify the image using the [Bits](../a-z/bits.md) and [CMap](../a-z/cmap.md) properties. The alternative is to use the [CBits](../a-z/cbits.md) property which works for any size of colour palette.


If [MaskCol](../a-z/maskcol.md) is non-zero, it specifies the transparent colour for the Bitmap. Any pixels specified with the same colour will instead be displayed in whatever colour is underneath the Bitmap. This achieves similar behaviour to that of an Icon.


The [KeepBits](../a-z/keepbits.md) property has the value 0 or 1, and controls how a Bitmap is saved in the workspace. A value of 0 (the default) means that the values of [CBits](../a-z/cbits.md), [Bits](../a-z/bits.md) and [CMap](../a-z/cmap.md) are **not** kept in the workspace. If you request the values of [CBits](../a-z/cbits.md), [Bits](../a-z/bits.md) or [CMap](../a-z/cmap.md) with [`⎕WG`](../../Language/System Functions/wg.htm), they are obtained directly from the corresponding Windows bitmap resource. When the workspace is `)LOAD`ed, the Bitmap is recreated from the associated file defined by the value of the [File](../a-z/file.md) property. Note that if this file doesn't exist when the workspace is `)LOAD`ed, the Bitmap is not created, but no error is generated. However, when you reference the object you will get a `VALUE ERROR`.


If [KeepBits](../a-z/keepbits.md) is 1, the values of [CBits](../a-z/cbits.md), [Bits](../a-z/bits.md) and [CMap](../a-z/cmap.md) **are** stored permanently in the workspace, and are used to rebuild the Bitmap when the workspace is `)LOAD`ed. In this case, the file name (if any) is ignored. Setting [KeepBits](../a-z/keepbits.md) to 1 uses more workspace, but may be more convenient if you want to distribute applications.


The [Size](../a-z/size.md) property allows you to query the size of a Bitmap without having to retrieve the [CBits](../a-z/cbits.md) or [Bits](../a-z/bits.md) property and then take its "shape". This will be noticeably faster for a large Bitmap. If you set the [Size](../a-z/size.md) property using [`⎕WS`](../../Language/System Functions/ws.htm) the Bitmap is scaled to the new size.


A useful feature of a Bitmap is that it can be the parent of any of the graphical objects. This allows you to create or edit a bitmap by drawing lines, circles, etc. in it.


The [FileRead](../a-z/fileread.md) (90) and [FileWrite](../a-z/filewrite.md) (91) methods allow you to dynamically manage bitmap files (.BMP). The expression:
```apl
      bmname.FileWrite
```


causes the Bitmap called `bmname` to be written to the file specified by the current value of the [File](../a-z/file.md) property. The file is automatically written in standard bitmap format. Similarly, the expression:
```apl
      bmname.FileRead
```


causes the Bitmap called `bmname` to be redefined from the bitmap file specified by the current value of the [File](../a-z/file.md) property.


The [MakeGIF](../a-z/makegif.md) and [MakePNG](../a-z/makepng.md) methods may be used to convert the image represented by a Bitmap object into a GIF or PNG data stream, suitable for display in a web browser. The [TCPSendPicture](../a-z/tcpsendpicture.md) method may be used to transfer a Bitmap on a TCP/IP socket.


Using a bitmap is always a 2-stage process. First you create a Bitmap object with [`⎕WC`](../../Language/System Functions/wc.htm). Then you use it by specifying its name as a property of another object.


The [Picture](../a-z/picture.md) property specifies the name of a Bitmap to be displayed in an [ActiveXControl](../a-z/activexcontrol.md), [Button](../a-z/button.md), [Form](../a-z/form.md), [Group](../a-z/group.md), [Image](../a-z/image.md), [MDIClient](../a-z/mdiclient.md), [Sm](../a-z/sm.md), [Static](../a-z/static.md), [StatusBar](../a-z/statusbar.md), [StatusField](../a-z/statusfield.md), [SubForm](../a-z/subform.md), [TabBar](../a-z/tabbar.md), or [ToolBar](../a-z/toolbar.md).


The [BtnPix](../a-z/btnpix.md) property specifies three Bitmaps to be used to represent the 3 states of a [Button](../a-z/button.md), [Menu](../a-z/menu.md) or [MenuItem](../a-z/menuitem.md).


The [FStyle](../a-z/fstyle.md) property specifies the name of a Bitmap to be used as a pattern to fill a [Poly](../a-z/poly.md), [Ellipse](../a-z/ellipse.md) or [Rect](../a-z/rect.md) object.


