




<h1 class="heading"><span class="name">Metafile</span></h1>

| [Parents](../ParentLists/Metafile.htm) | [Children](../ChildLists/Metafile.htm) | [Properties](../PropLists/Metafile.htm) | [Methods](../MethodLists/Metafile.htm) | [Events](../EventLists/Metafile.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | This object represents a picture in Windows Metafile format. |
| --- | ---  |


**Description**


The Windows Metafile is a mechanism for representing a picture in terms of a collection of graphical components. Windows Metafiles are distributed in special files (.WMF) from which they are loaded into memory for use by an application. Once loaded a Metafile is a Windows "resource" that can be used in a variety of ways. The Metafile object represents this resource.



The [File](../a-z/file.md) property specifies the name of a .WMF file from which the Metafile is to be loaded or to which it is to be saved. If you specify [File](../a-z/file.md) with [`⎕WC`](../../Language/System Functions/wc.htm) the Metafile object is loaded from it. If you specify [File](../a-z/file.md) with [`⎕WS`](../../Language/System Functions/ws.htm) no action takes place until you instruct the Metafile object to re-initialise itself from the file or to save itself to the file. These operations are performed using the [FileRead](../a-z/fileread.md) and [FileWrite](../a-z/filewrite.md) methods. If you omit the [File](../a-z/file.md) property in the argument to [`⎕WC`](../../Language/System Functions/wc.htm) or if you specify a null vector, the Metafile object is initially empty. The following example loads the picture defined by the GOLF.WMF Metafile that is distributed with Microsoft Office.
```apl
      'GOLF' ⎕WC 'Metafile' 'C:\MSOFFICE\CLIPART\GOLF'
```


Whether or not the Metafile object is initialised from a file, you can add graphical components to it by creating child objects. However the Metafile behaves like a [Bitmap](../a-z/bitmap.md) object in that its children cannot be modified using [`⎕WS`](../../Language/System Functions/ws.htm) nor can they be removed using `⎕EX`. The components of a Metafile that has been initialised from a .WMF file also cannot be referenced in any way. It is therefore recommended that you use unnamed objects when you create the graphical components of a Metafile.


The following statements create an empty Metafile called `MF` and then draw a line and circle in it.
```apl
      'MF' ⎕WC 'Metafile'
      'MF.' ⎕WC 'Poly' (50(10 90))
      'MF.' ⎕WC 'Circle' (50 50) 30
```


Like the [Bitmap](../a-z/bitmap.md), [Icon](../a-z/icon.md), [Font](../a-z/font.md) and [Cursor](../a-z/cursor.md) objects, the Metafile is a resource that is not visible until it is *used*. This is done by setting the [Picture](../a-z/picture.md) property of another object ([Form](../a-z/form.md), [Image](../a-z/image.md), [Static](../a-z/static.md) or [SubForm](../a-z/subform.md)) to the name of, or ref to, the Metafile object. For example, to display the Metafile `MF` in a [Form](../a-z/form.md), you could type :
```apl
      'TEST' ⎕WC 'FORM' ('Picture' 'MF')
```


You can also copy a Metafile object to the Windows Clipboard from where it can be pasted into another application. This is done by creating a [Clipboard](../a-z/clipboard.md) object and then setting its [MetafileObj](../a-z/metafileobj.md) property to the name of the Metafile object to be exported. For example :
```apl
      'CL' ⎕WC 'Clipboard'
      'CL' ⎕WS 'MetafileObj' 'MF'
```


The [FileWrite](../a-z/filewrite.md) method may be used to save a Metafile object on a file. The following statements save the Metafile `MF` in a file called TEST.WMF.
```apl
      MF.File←TEST'
      MF.FileWrite
```


The [Size](../a-z/size.md) property determines the granularity of  the Metafile. Its default value is the size of its parent. If you intend to replay the Metafile at higher resolution, you should set [Size](../a-z/size.md) accordingly.


The [RealSize](../a-z/realsize.md) property specifies the suggested size of a Metafile in units of 0.01mm. Setting [RealSize](../a-z/realsize.md) has the effect of making the Metafile *placeable*. Certain programs (such as Word for Windows) only support placeable metafiles.


