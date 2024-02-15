




<h1 class="heading"><span class="name">ImageList</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | The ImageList object represents a set of bitmapped images. |
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


An ImageList object represents an array of bitmapped images which are used to depict items in a ListView or TreeView object, or the images in a CoolBar, Menu, TabControl or ToolControl.



Making an ImageList is a 2-step process. First, you create an (empty) ImageList specifying its [Size](./size.md) and [Masked](./masked.md) properties. The former establishes the size of each of the bitmapped images in the array. The [Masked](./masked.md) property specifies whether the ImageList is to contain opaque or transparent images. Note that these properties must be established when the ImageList is created by `⎕WC` and may not subsequently be changed using `⎕WS`.


Next, you create a series of Bitmap or Icon objects as *children* of the ImageList. As you make each one, APL adds the corresponding image (or images) to the ImageList object. If the size of each of the Bitmap or Icon objects is equal to the [Size](./size.md) of the ImageList itself, each child object corresponds to an image in the ImageList. However, if you add an object whose *width* is an exact multiple of the *width* of the ImageList, a corresponding number of images will be added.


For example, if the [Size](./size.md) of the ImageList is 16x16 (the default) and you create a child Bitmap of size 16x48, three images (each of size 16x16) will be added to the ImageList. This is more efficient than building the images one-by-one. In other circumstances (where the size of the Bitmap or Icon is not equal to [Size](./size.md) of ImageList), the Bitmap or Icon will be scaled to fit.


Note that when making Bitmaps or Icons as children of an ImageList, it is not necessary to *name* them because they are subsequently referenced only via the [ImageIndex](./imageindex.md) and [SelImageIndex](./selimageindex.md) properties and not by name. The number of images in an ImageList is given by the read-only property, ImageCount.


The [MapCols](./mapcols.md) property, which must be specified at the time you create the object, specifies whether or not bitmap colours are remapped to reflect the user's colour preferences.


An ImageList is *associated* with a ListView or TreeView object by the [ImageListObj](./imagelistobj.md) property. Each item in the ListView or TreeView is then allocated a specific image in the ImageList by the [ImageIndex](./imageindex.md) and [SelImageIndex](./selimageindex.md) properties.

