




<h1 class="heading"><span class="name">ImageList</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | The ImageList object represents a set of bitmapped images. |
| --- | --- | ---  |
| Parents | [Detach](../a-z/detach.md) | [Detach](../a-z/detach.md) |  |  |
| [Detach](../a-z/detach.md) |  |  |
| Children | [Detach](../a-z/detach.md) | [Detach](../a-z/detach.md) |  |  |
| [Detach](../a-z/detach.md) |  |  |
| Properties | [Detach](../a-z/detach.md) | [Detach](../a-z/detach.md) |  |  |
| [Detach](../a-z/detach.md) |  |  |
| Methods | [Detach](../a-z/detach.md) | [Detach](../a-z/detach.md) |  |  |
| [Detach](../a-z/detach.md) |  |  |
| Events | [Detach](../a-z/detach.md) | [Detach](../a-z/detach.md) |  |  |
| [Detach](../a-z/detach.md) |  |  |


Description


An ImageList object represents an array of bitmapped images which are used to depict items in a [ListView](../a-z/listview.md) or [TreeView](../a-z/treeview.md) object, or the images in a [CoolBar](../a-z/coolbar.md), [Menu](../a-z/menu.md), [TabControl](../a-z/tabcontrol.md) or [ToolControl](../a-z/toolcontrol.md).



Making an ImageList is a 2-step process. First, you create an (empty) ImageList specifying its [Size](../a-z/size.md) and [Masked](../a-z/masked.md) properties. The former establishes the size of each of the bitmapped images in the array. The [Masked](../a-z/masked.md) property specifies whether the ImageList is to contain opaque or transparent images. Note that these properties must be established when the ImageList is created by `⎕WC` and may not subsequently be changed using `⎕WS`.


Next, you create a series of [Bitmap](../a-z/bitmap.md) or [Icon](../a-z/icon.md) objects as *children* of the ImageList. As you make each one, APL adds the corresponding image (or images) to the ImageList object. If the size of each of the [Bitmap](../a-z/bitmap.md) or [Icon](../a-z/icon.md) objects is equal to the [Size](../a-z/size.md) of the ImageList itself, each child object corresponds to an image in the ImageList. However, if you add an object whose *width* is an exact multiple of the *width* of the ImageList, a corresponding number of images will be added.


For example, if the [Size](../a-z/size.md) of the ImageList is 16x16 (the default) and you create a child [Bitmap](../a-z/bitmap.md) of size 16x48, three images (each of size 16x16) will be added to the ImageList. This is more efficient than building the images one-by-one. In other circumstances (where the size of the [Bitmap](../a-z/bitmap.md) or [Icon](../a-z/icon.md) is not equal to [Size](../a-z/size.md) of ImageList), the [Bitmap](../a-z/bitmap.md) or [Icon](../a-z/icon.md) will be scaled to fit.


Note that when making Bitmaps or Icons as children of an ImageList, it is not necessary to *name* them because they are subsequently referenced only via the [ImageIndex](../a-z/imageindex.md) and [SelImageIndex](../a-z/selimageindex.md) properties and not by name. The number of images in an ImageList is given by the read-only property, ImageCount.


The [MapCols](../a-z/mapcols.md) property, which must be specified at the time you create the object, specifies whether or not bitmap colours are remapped to reflect the user's colour preferences.


An ImageList is *associated* with a [ListView](../a-z/listview.md) or [TreeView](../a-z/treeview.md) object by the [ImageListObj](../a-z/imagelistobj.md) property. Each item in the [ListView](../a-z/listview.md) or [TreeView](../a-z/treeview.md) is then allocated a specific image in the ImageList by the [ImageIndex](../a-z/imageindex.md) and [SelImageIndex](../a-z/selimageindex.md) properties.


