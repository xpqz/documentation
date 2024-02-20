




<h1 class="heading"><span class="name">File</span></h1>

**Applies To**


**Description**


Specifies the name of a file associated with an object.



For an [Animation](./animation.md), [Bitmap](./bitmap.md), [Cursor](./cursor.md) or [Icon](./icon.md) object, this property is either a simple character vector or a 2-element nested vector.


If it is simple, File specifies the name of the associated bitmap (.BMP), icon (.ICO) or cursor (.CUR) file.


If it is nested, the first element specifies the name of a DLL or ([Icon](./icon.md) only) EXE and the second element identifies the particular bitmap, icon or cursor in that file. The identifier may be its *name* (a character string), its *resource id* (a non-zero positive integer) or ([Icon](./icon.md) only), its *index* (0 or negative integer) within the file. As a special case, if the name of the file is an empty vector, the object is loaded from DYALOG.EXE or the Dyalog resource DLL. The name of the latter varies according to the version installed but begins DYARES. In this case, the identifier must be a name or resource id; indexes are not supported.


For a [Metafile](./metafile.md) object, File must be simple and specifies the name of a metafile (.WMF) file. For a [RichEdit](./richedit.md) object, File must be simple and specifies the name of a Rich text Format (.RTF) file.


When applied to a [FileBox](./filebox.md) object, File contains the name (or names) of the selected file (or files) depending upon the value of its [Style](style.md) (`'Single'` or `'Multi').`


