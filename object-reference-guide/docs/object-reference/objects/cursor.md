




<h1 class="heading"><span class="name">Cursor</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | This object defines a cursor. |
| --- | --- | ---  |
| Parents | [Detach](../a-z/detach.md) [FileRead](../a-z/fileread.md) [FileWrite](../a-z/filewrite.md) | [Detach](../a-z/detach.md) | [FileRead](../a-z/fileread.md) | [FileWrite](../a-z/filewrite.md) |
| [Detach](../a-z/detach.md) | [FileRead](../a-z/fileread.md) | [FileWrite](../a-z/filewrite.md) |
| Children | [Detach](../a-z/detach.md) [FileRead](../a-z/fileread.md) [FileWrite](../a-z/filewrite.md) | [Detach](../a-z/detach.md) | [FileRead](../a-z/fileread.md) | [FileWrite](../a-z/filewrite.md) |
| [Detach](../a-z/detach.md) | [FileRead](../a-z/fileread.md) | [FileWrite](../a-z/filewrite.md) |
| Properties | [Detach](../a-z/detach.md) [FileRead](../a-z/fileread.md) [FileWrite](../a-z/filewrite.md) | [Detach](../a-z/detach.md) | [FileRead](../a-z/fileread.md) | [FileWrite](../a-z/filewrite.md) |
| [Detach](../a-z/detach.md) | [FileRead](../a-z/fileread.md) | [FileWrite](../a-z/filewrite.md) |
| Methods | [Detach](../a-z/detach.md) [FileRead](../a-z/fileread.md) [FileWrite](../a-z/filewrite.md) | [Detach](../a-z/detach.md) | [FileRead](../a-z/fileread.md) | [FileWrite](../a-z/filewrite.md) |
| [Detach](../a-z/detach.md) | [FileRead](../a-z/fileread.md) | [FileWrite](../a-z/filewrite.md) |
| Events | [Detach](../a-z/detach.md) [FileRead](../a-z/fileread.md) [FileWrite](../a-z/filewrite.md) | [Detach](../a-z/detach.md) | [FileRead](../a-z/fileread.md) | [FileWrite](../a-z/filewrite.md) |
| [Detach](../a-z/detach.md) | [FileRead](../a-z/fileread.md) | [FileWrite](../a-z/filewrite.md) |


Description


The [File](../a-z/file.md) property defines the name of a cursor file associated with the Cursor object, or it specifies the name of a DLL and the resource number or name of the cursor therein. If you omit the file extension, the system assumes .CUR. To use an animated cursor you must therefore specify the .AMI extension explicitly.



If the value of the [File](../a-z/file.md) property is set by `⎕WS`, no immediate action is taken, but the corresponding file may subsequently be read or written using the [FileRead](../a-z/fileread.md) or [FileWrite](../a-z/filewrite.md) methods.


The [Bits](../a-z/bits.md) and [Mask](../a-z/mask.md) properties define the appearance of the cursor. Both are Boolean matrices with a shape of 32  32. The colour of each pixel in the cursor is defined by the following table. Note that a 0 in [Bits](../a-z/bits.md) combined with a 1 in [Mask](../a-z/mask.md) causes the corresponding pixel to be the colour of the background. This is used to give the cursor a non-rectangular shape.

| Bits | 0 | 1 | 0 | 1 |
| --- | --- | --- | --- | ---  |
| Mask | 0 | 0 | 1 | 1 |
| Pixel | Black | White | Background | Inverse |


The [HotSpot](../a-z/hotspot.md) property determines the point within the cursor that registers its position over another object.


A Cursor is used by setting the [CursorObj](../a-z/cursorobj.md) property of another object to its name or ref.


