




<h1 class="heading"><span class="name">Image</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | Positions bitmaps and icons within an object. |
| --- | --- | ---  |
| Parents | [Detach](./detach.md) | [Detach](./detach.md) |  |  |
| [Detach](./detach.md) |  |  |
| Children | [Detach](./detach.md) | [Detach](./detach.md) |  |  |
| [Detach](./detach.md) |  |  |
| Properties | [Detach](./detach.md) | [Detach](./detach.md) |  |  |
| [Detach](./detach.md) |  |  |
| Methods | [Detach](./detach.md) | [Detach](./detach.md) |  |  |
| [Detach](./detach.md) |  |  |
| Events | [Detach](./detach.md) | [Detach](./detach.md) |  |  |
| [Detach](./detach.md) |  |  |


Description


The [Points](./points.md) property specifies the co-ordinates of one or more points at which the specified graphical objects are to be drawn.



The [Picture](./picture.md) property specifies the name(s) of Bitmap, [Icon](icon.md) or Metafile object(s) that are to be drawn. It may be a simple character vector or a vector of vectors.


To draw a single graphic picture, the [Picture](./picture.md) property is a simple character vector specifying the name of a Bitmap, [Icon](icon.md) or Metafile object. [Points](./points.md) is either a 2-element vector or a 1-row, 2-column matrix whose elements specify the y-coordinate and x-coordinate respectively at which the object is to be drawn.


To draw the same picture at several different positions, the [Picture](./picture.md) property is a simple character vector specifying the name of the Bitmap, [Icon](icon.md) or Metafile object. [Points](./points.md) is either a 2-column matrix of y-coordinates and x-coordinates, or a nested vector whose first element contains the y-coordinates and whose second element contains the x-coordinates.


To draw several different pictures, the [Picture](./picture.md) property is a vector of character vectors specifying the names of several Bitmap, [Icon](icon.md) and/or Metafile objects. [Points](./points.md) is a 2-column matrix or 2-element nested vector as described above.


Setting the [EdgeStyle](./edgestyle.md) property causes the picture to be surrounded by the appropriate border. For example, setting [EdgeStyle](./edgestyle.md) to `'Plinth'` produces a button-like appearance.


Setting the [Size](./size.md) property causes the picture to be scaled to fit within the specified rectangle. It is only necessary to specify [Size](./size.md) when an Image is used to draw a Metafile object. For a Bitmap or [Icon](icon.md), [Size](./size.md) defaults to the size of the object being drawn.


The [Dragable](./dragable.md) property specifies whether or not the Image can be dragged and dropped using the mouse.

#### Examples:


First make a Form
```apl
      'F' ⎕WC 'Form'
```


Then make two Bitmaps :
```apl
      'YES' ⎕WC 'Bitmap' 'C:\WDYALOG\WS\YES'
      'NO'  ⎕WC 'Bitmap' 'C:\WDYALOG\WS\NO'
```


Display the "YES" Bitmap at (20,10)
```apl
      'F.I' ⎕WC 'Image' (20 10)('Picture' 'YES')
```


Display the "YES" Bitmap at (20,10) and (20,50)
```apl
      'F.I' ⎕WC 'Image' (20(10 50))('Picture' 'YES')
```


Display the "YES" Bitmap at (20,10) and the "NO" Bitmap at (20,50)
```apl
      'F.I' ⎕WC'Image'(20(10 50))('Picture' 'YES' 'NO')
```

