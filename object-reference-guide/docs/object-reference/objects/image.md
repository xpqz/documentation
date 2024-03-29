




<h1 class="heading"><span class="name">Image</span></h1>

[Parents](../ParentLists/Image.htm) [Children](../ChildLists/Image.htm) [Properties](../PropLists/Image.htm) [Methods](../MethodLists/Image.htm) [Events](../EventLists/Image.htm)


Purpose: Positions bitmaps and icons within an object.


**Description**


The [Points](../a-z/points.md) property specifies the co-ordinates of one or more points at which the specified graphical objects are to be drawn.



The [Picture](../a-z/picture.md) property specifies the name(s) of [Bitmap](../a-z/bitmap.md), [Icon](../a-z/icon.md) or [Metafile](../a-z/metafile.md) object(s) that are to be drawn. It may be a simple character vector or a vector of vectors.


To draw a single graphic picture, the [Picture](../a-z/picture.md) property is a simple character vector specifying the name of a [Bitmap](../a-z/bitmap.md), [Icon](../a-z/icon.md) or [Metafile](../a-z/metafile.md) object. [Points](../a-z/points.md) is either a 2-element vector or a 1-row, 2-column matrix whose elements specify the y-coordinate and x-coordinate respectively at which the object is to be drawn.


To draw the same picture at several different positions, the [Picture](../a-z/picture.md) property is a simple character vector specifying the name of the [Bitmap](../a-z/bitmap.md), [Icon](../a-z/icon.md) or [Metafile](../a-z/metafile.md) object. [Points](../a-z/points.md) is either a 2-column matrix of y-coordinates and x-coordinates, or a nested vector whose first element contains the y-coordinates and whose second element contains the x-coordinates.


To draw several different pictures, the [Picture](../a-z/picture.md) property is a vector of character vectors specifying the names of several [Bitmap](../a-z/bitmap.md), [Icon](../a-z/icon.md) and/or [Metafile](../a-z/metafile.md) objects. [Points](../a-z/points.md) is a 2-column matrix or 2-element nested vector as described above.


Setting the [EdgeStyle](../a-z/edgestyle.md) property causes the picture to be surrounded by the appropriate border. For example, setting [EdgeStyle](../a-z/edgestyle.md) to `'Plinth'` produces a button-like appearance.


Setting the [Size](../a-z/size.md) property causes the picture to be scaled to fit within the specified rectangle. It is only necessary to specify [Size](../a-z/size.md) when an Image is used to draw a [Metafile](../a-z/metafile.md) object. For a [Bitmap](../a-z/bitmap.md) or [Icon](../a-z/icon.md), [Size](../a-z/size.md) defaults to the size of the object being drawn.


The [Dragable](../a-z/dragable.md) property specifies whether or not the Image can be dragged and dropped using the mouse.

#### Examples:


First make a [Form](../a-z/form.md)
```apl
      'F' ⎕WC 'Form'
```


Then make two [Bitmap](../a-z/bitmap.md)s :
```apl
      'YES' ⎕WC 'Bitmap' 'C:\WDYALOG\WS\YES'
      'NO'  ⎕WC 'Bitmap' 'C:\WDYALOG\WS\NO'
```


Display the "YES" [Bitmap](../a-z/bitmap.md) at (20,10)
```apl
      'F.I' ⎕WC 'Image' (20 10)('Picture' 'YES')
```


Display the "YES" [Bitmap](../a-z/bitmap.md) at (20,10) and (20,50)
```apl
      'F.I' ⎕WC 'Image' (20(10 50))('Picture' 'YES')
```


Display the "YES" [Bitmap](../a-z/bitmap.md) at (20,10) and the "NO" [Bitmap](../a-z/bitmap.md) at (20,50)
```apl
      'F.I' ⎕WC'Image'(20(10 50))('Picture' 'YES' 'NO')
```


