




<h1 class="heading"><span class="name">Metafile</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | This object represents a picture in Windows Metafile format. |
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


The Windows Metafile is a mechanism for representing a picture in terms of a collection of graphical components. Windows Metafiles are distributed in special files (.WMF) from which they are loaded into memory for use by an application. Once loaded a Metafile is a Windows "resource" that can be used in a variety of ways. The Metafile object represents this resource.



The [File](./file.md) property specifies the name of a .WMF file from which the Metafile is to be loaded or to which it is to be saved. If you specify [File](./file.md) with `⎕WC` the Metafile object is loaded from it. If you specify [File](./file.md) with `⎕WS` no action takes place until you instruct the Metafile object to re-initialise itself from the file or to save itself to the file. These operations are performed using the [FileRead](./fileread.md) and [FileWrite](./filewrite.md) methods. If you omit the [File](./file.md) property in the argument to `⎕WC` or if you specify a null vector, the Metafile object is initially empty. The following example loads the picture defined by the GOLF.WMF Metafile that is distributed with Microsoft Office.
```apl
      'GOLF' ⎕WC 'Metafile' 'C:\MSOFFICE\CLIPART\GOLF'
```


Whether or not the Metafile object is initialised from a file, you can add graphical components to it by creating child objects. However the Metafile behaves like a [Bitmap](bitmap.md) object in that its children cannot be modified using `⎕WS` nor can they be removed using `⎕EX`. The components of a Metafile that has been initialised from a .WMF file also cannot be referenced in any way. It is therefore recommended that you use unnamed objects when you create the graphical components of a Metafile.


The following statements create an empty Metafile called `MF` and then draw a line and circle in it.
```apl
      'MF' ⎕WC 'Metafile'
      'MF.' ⎕WC 'Poly' (50(10 90))
      'MF.' ⎕WC 'Circle' (50 50) 30
```


Like the [Bitmap](bitmap.md), [Icon](icon.md), [Font](font.md) and [Cursor](cursor.md) objects, the Metafile is a resource that is not visible until it is *used*. This is done by setting the [Picture](./picture.md) property of another object ([Form](form.md), [Image](image.md), [Static](static.md) or [SubForm](subform.md)) to the name of, or ref to, the Metafile object. For example, to display the Metafile `MF` in a [Form](form.md), you could type :
```apl
      'TEST' ⎕WC 'FORM' ('Picture' 'MF')
```


You can also copy a Metafile object to the Windows Clipboard from where it can be pasted into another application. This is done by creating a [Clipboard](clipboard.md) object and then setting its [MetafileObj](./metafileobj.md) property to the name of the Metafile object to be exported. For example :
```apl
      'CL' ⎕WC 'Clipboard'
      'CL' ⎕WS 'MetafileObj' 'MF'
```


The [FileWrite](./filewrite.md) method may be used to save a Metafile object on a file. The following statements save the Metafile `MF` in a file called TEST.WMF.
```apl
      MF.File←TEST'
      MF.FileWrite
```


The [Size](./size.md) property determines the granularity of  the Metafile. Its default value is the size of its parent. If you intend to replay the Metafile at higher resolution, you should set [Size](./size.md) accordingly.


The [RealSize](./realsize.md) property specifies the suggested size of a Metafile in units of 0.01mm. Setting [RealSize](./realsize.md) has the effect of making the Metafile *placeable*. Certain programs (such as Word for Windows) only support placeable metafiles.


