




<h1 class="heading"><span class="name">FileRead</span></h1>
| Applies To: | [Bitmap](../a-z/bitmap.md) | [Cursor](../a-z/cursor.md) | [Icon](../a-z/icon.md) | [Metafile](../a-z/metafile.md) | [RichEdit](../a-z/richedit.md) |
| --- | --- | --- | --- | --- | ---  |

| Applies To: | [Bitmap](../a-z/bitmap.md) [Cursor](../a-z/cursor.md) [Icon](../a-z/icon.md) [Metafile](../a-z/metafile.md) [RichEdit](../a-z/richedit.md) | [Bitmap](../a-z/bitmap.md) | [Cursor](../a-z/cursor.md) | [Icon](../a-z/icon.md) | [Metafile](../a-z/metafile.md) | [RichEdit](../a-z/richedit.md) |  |
| --- | --- | ---  |
| [Bitmap](../a-z/bitmap.md) | [Cursor](../a-z/cursor.md) | [Icon](../a-z/icon.md) |
| [Metafile](../a-z/metafile.md) | [RichEdit](../a-z/richedit.md) |  |


Description


This method causes the object to be recreated from the file named in its [File](../a-z/file.md) property.


The FileRead method is niladic.

| `[1]` | Object | ref or character vector |
| --- | --- | ---  |
| `[2]` | Event | `'FileRead'` or 90 |


If you attach a callback function to this event and have it return a value of 0, the object will not be recreated from file.



