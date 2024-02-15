




<h1 class="heading"><span class="name">FileWrite</span></h1>
| Applies To: | [Bitmap](../a-z/bitmap.md) | [Cursor](../a-z/cursor.md) | [Icon](../a-z/icon.md) | [Metafile](../a-z/metafile.md) | [RichEdit](../a-z/richedit.md) |
| --- | --- | --- | --- | --- | ---  |

| Applies To: | [Bitmap](../a-z/bitmap.md) [Cursor](../a-z/cursor.md) [Icon](../a-z/icon.md) [Metafile](../a-z/metafile.md) [RichEdit](../a-z/richedit.md) | [Bitmap](../a-z/bitmap.md) | [Cursor](../a-z/cursor.md) | [Icon](../a-z/icon.md) | [Metafile](../a-z/metafile.md) | [RichEdit](../a-z/richedit.md) |  |
| --- | --- | ---  |
| [Bitmap](../a-z/bitmap.md) | [Cursor](../a-z/cursor.md) | [Icon](../a-z/icon.md) |
| [Metafile](../a-z/metafile.md) | [RichEdit](../a-z/richedit.md) |  |


Description


This method causes the object to be written to the file named in its [File](../a-z/file.md) property. For the Bitmap and Icon objects this method will write a file of type .BMP and .ICO to a file with the appropriate extension. If [File](../a-z/file.md) specifies any other extension, the method will fail with a `DOMAIN ERROR`:
```apl
 DOMAIN ERROR: This object cannot be saved to this type of file.
```


The FileWrite method is niladic.


If you attach a callback function to this event and have it return a value of 0, the object will not be written to file. You could use this to avoid overwriting an existing file.



