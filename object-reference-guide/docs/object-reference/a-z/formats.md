




<h1 class="heading"><span class="name">Formats</span></h1>

Applies To: [Clipboard](./clipboard.md)


**Description**


This is a "read-only" property that identifies the formats in which data is currently available in the clipboard. It is a vector of character vectors containing the names of the corresponding [Clipboard](./clipboard.md) properties for which data may be obtained using [`⎕WG`](../../Language/System Functions/wg.htm). In the following example data was copied to the Windows clipboard from Microsoft Excel. This product stores data in CF_Text and the older device-dependent CF_Bitmap formats. The latter excludes colour map information, so [CMap](cmap.md) is not available.
```apl
      'CL' ⎕WC 'Clipboard'
      'CL' ⎕WG 'Formats'
 Bits  CMap  Text
```



