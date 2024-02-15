




<h1 class="heading"><span class="name">FileWrite</span></h1>

| Applies To: | [Bitmap](./bitmap.md) | [Cursor](./cursor.md) | [Icon](./icon.md) | [Metafile](./metafile.md) | [RichEdit](./richedit.md) |
| --- | --- | --- | --- | --- | ---  |


**Description**


This method causes the object to be written to the file named in its [File](./file.md) property. For the Bitmap and Icon objects this method will write a file of type .BMP and .ICO to a file with the appropriate extension. If [File](./file.md) specifies any other extension, the method will fail with a `DOMAIN ERROR`:
```apl
 DOMAIN ERROR: This object cannot be saved to this type of file.
```


The FileWrite method is niladic.


If you attach a callback function to this event and have it return a value of 0, the object will not be written to file. You could use this to avoid overwriting an existing file.



