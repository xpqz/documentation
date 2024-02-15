




<h1 class="heading"><span class="name">Clipboard</span></h1>

| [Parents](../ParentLists/Clipboard.htm) | [Children](../ChildLists/Clipboard.htm) | [Properties](../PropLists/Clipboard.htm) | [Methods](../MethodLists/Clipboard.htm) | [Events](../EventLists/Clipboard.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | This object provides access to the Windows clipboard. |
| --- | ---  |


**Description**


When an application places data in the Windows clipboard, it may store it in one or more formats. An application wishing to retrieve data from the clipboard can then choose which format to read it in. Dyalog APL supports standard clipboard formats, including CF_TEXT, CF_BITMAP and CF_METAFILE. If there is any data in the clipboard, the [Formats](./formats.md) property lists the formats in which it may be retrieved.



In addition, the [Array](./array.md) property may be used to set or retrieve clipboard contents in Dyalog APL array format.


Data is read from the clipboard using [`⎕WG`](../../Language/System%20Functions/wg.htm), specifying the name of the appropriate property for the data that you want.


If the data has been stored in CF_Text format, the value of [Formats](./formats.md) will include `'Text'` and you may retrieve the data by querying the value of the [Text](./text.md) property with [`⎕WG`](../../Language/System%20Functions/wg.htm).


If the data has been stored in **device-independent** bitmap format, the value of [Formats](./formats.md) will include `'CBits'`, `'Bits'` and `'CMap'`. To retrieve the bitmap pattern and colour map, you may query the values of the [CBits](./cbits.md), or [Bits](./bits.md) and [CMap](./cmap.md) properties using [`⎕WG`](../../Language/System%20Functions/wg.htm).


If the data has been stored in **device-dependent** bitmap format, only the bitmap pattern is available and [Formats](./formats.md) will contain `'Bits'` but not `'CMap'`. In this case you can query the [Bits](./bits.md) property but not [CMap](./cmap.md) without which you cannot realise the bitmap. However, if data was posted in this format, it is highly probable that the current Windows colour map applies to it. For a standard 16-colour device this is given under the description of the [CMap](./cmap.md) property.



The following example retrieves text from the clipboard :
```apl
      'CL' ⎕WC 'Clipboard'
      Data ← 'CL' ⎕WG 'Text'
```




The next example retrieves a bitmap from the clipboard and defines it as a [Bitmap](bitmap.md) object named `'BM'` ready for use :
```apl
      'BM' ⎕WC 'Bitmap' '', 'CL' ⎕WG 'Bits' 'CMap'
```




Data may be placed in the clipboard using [`⎕WC`](../../Language/System%20Functions/wc.htm) or [`⎕WS`](../../Language/System%20Functions/ws.htm). To store text, you simply set the [Text](./text.md) property. You may use a simple character vector or matrix, or a vector of character vectors. For example :
```apl
      'CL' ⎕WS 'Text' 'Hello World'
```




To store a bitmap you can set either the [Picture](./picture.md) property to the **name** of a [Bitmap](bitmap.md) object, or you can set the [Bits](./bits.md) and [CMap](./cmap.md) properties explicitly. The former is more efficient, especially for large bitmaps, for example :
```apl
      'CL' ⎕WS 'Bitmap' 'BM'
```


or
```apl
      Bits CMap ← 'BM' ⎕WG 'Bits' 'CMap'
      'CL' ⎕WS ('Bits' Bits)('CMap' CMap)
```



Note that if you use the latter method, you must set **both** properties in one [`⎕WS`](../../Language/System%20Functions/ws.htm) statement. This is also true if you wish to store data in both Text and Bitmap formats together.


The [Metafile](./metafileobj.md) property allows graphical information to be restored in and retrieved from the clipboard in Windows Metafile format. See the description of the [Metafile](./metafileobj.md) property for details.


A [ClipChange](./clipchange.md) (120) event is generated when another application places data in the clipboard.


