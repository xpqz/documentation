




<h1 class="heading"><span class="name">FileRead</span></h1>
| Applies To: | [Bitmap](./bitmap.md) | [Cursor](./cursor.md) | [Icon](./icon.md) | [Metafile](./metafile.md) | [RichEdit](./richedit.md) |
| --- | --- | --- | --- | --- | ---  |

| Applies To: | [Bitmap](./bitmap.md) [Cursor](./cursor.md) [Icon](./icon.md) [Metafile](./metafile.md) [RichEdit](./richedit.md) | [Bitmap](./bitmap.md) | [Cursor](./cursor.md) | [Icon](./icon.md) | [Metafile](./metafile.md) | [RichEdit](./richedit.md) |  |
| --- | --- | ---  |
| [Bitmap](./bitmap.md) | [Cursor](./cursor.md) | [Icon](./icon.md) |
| [Metafile](./metafile.md) | [RichEdit](./richedit.md) |  |


Description


This method causes the object to be recreated from the file named in its [File](./file.md) property.


The FileRead method is niladic.

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'FileRead'` or 90 |


If you attach a callback function to this event and have it return a value of 0, the object will not be recreated from file.



