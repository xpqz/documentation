




<h1 class="heading"><span class="name">MetafileObj</span></h1>

| Applies To: | [Clipboard](../a-z/clipboard.md) |
| --- | ---  |


**Description**


This property is used to copy graphical data to and from the Windows clipboard using the Windows Metafile format.



When you set the MetafileObj property of a [Clipboard](../a-z/clipboard.md) object to the name of the [Metafile](../a-z/metafile.md) object using [`⎕WS`](../../Language/System%20Functions/ws.htm) its contents are copied to the Windows clipboard in Windows Metafile format.


To import a picture that has been stored in the Windows clipboard in Metafile format you use [`⎕WG`](../../Language/System%20Functions/wg.htm). This returns a nested array whose elements correspond to the graphical components of the picture. Each of the elements of the array may be used as the arguments of [`⎕WC`](../../Language/System%20Functions/wc.htm) to draw the corresponding component of the picture. For example, if the picture stored in C:\MSOFFICE\CLIPART\BIRD.WMF is copied to the Windows clipboard, it may be imported into Dyalog APL/W as follows :
```apl
      BIRD ← 'CL' ⎕WG 'MetafileObj'
      ⍴BIRD
4
```


Each of the items in `BIRD` is a 2-element vector. The first element is a "dummy" object name which you may use or ignore as you wish. The second element is an array that defines a graphical object and is suitable as the right argument of [`⎕WC`](../../Language/System%20Functions/wc.htm). For example :
```apl
      2⊃4⊃BIRD
POLY  191 397   FSTYLE  0   FILLCOL  0 0 0    ...

190 402
187 406
182 409
176 410
172 409
168 406
165 402
164 397
165 391
168 387
172 384
176 383
182 384
187 387
190 391
191 397
189 395
191 397
```


From this array, you can rebuild the imported picture component by component, either as a [Metafile](../a-z/metafile.md) object or directly onto a [Form](../a-z/form.md), [Static](../a-z/static.md) or another object. The following example draws the picture in a [Form](../a-z/form.md) using the dummy names supplied.
```apl
      'TEST' ⎕WC 'FORM' ('Coord' 'User')
      'TEST' ⎕WS ('YRange' 0 1024)('XRange' 0 2048)
      TEST.⎕WC/¨BIRD
```


Notice that the co-ordinates of each of the graphical components are typically integers in a co-ordinate system that extends from 0 to 1024 in the y-direction and 0 to 2048 in the x-direction. The simplest way to draw the picture is therefore to set up the same co-ordinate system on a [Form](../a-z/form.md) as in the example above.


