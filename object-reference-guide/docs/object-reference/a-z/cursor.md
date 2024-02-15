




<h1 class="heading"><span class="name">Cursor</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | This object defines a cursor. |
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


The [File](./file.md) property defines the name of a cursor file associated with the Cursor object, or it specifies the name of a DLL and the resource number or name of the cursor therein. If you omit the file extension, the system assumes .CUR. To use an animated cursor you must therefore specify the .AMI extension explicitly.



If the value of the [File](./file.md) property is set by `⎕WS`, no immediate action is taken, but the corresponding file may subsequently be read or written using the [FileRead](./fileread.md) or [FileWrite](./filewrite.md) methods.


The [Bits](./bits.md) and [Mask](./mask.md) properties define the appearance of the cursor. Both are Boolean matrices with a shape of 32  32. The colour of each pixel in the cursor is defined by the following table. Note that a 0 in [Bits](./bits.md) combined with a 1 in [Mask](./mask.md) causes the corresponding pixel to be the colour of the background. This is used to give the cursor a non-rectangular shape.

| Bits | 0 | 1 | 0 | 1 |
| --- | --- | --- | --- | ---  |
| Mask | 0 | 0 | 1 | 1 |
| Pixel | Black | White | Background | Inverse |


The [HotSpot](./hotspot.md) property determines the point within the cursor that registers its position over another object.


A Cursor is used by setting the [CursorObj](./cursorobj.md) property of another object to its name or ref.


