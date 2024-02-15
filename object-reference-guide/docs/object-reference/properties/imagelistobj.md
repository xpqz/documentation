




<h1 class="heading"><span class="name">ImageListObj</span></h1>

**Applies To**


**Description**


The ImageListObj property is a simple character vector or a ref, or a vector of character vectors or refs that specifies [ImageList](../a-z/imagelist.md) objects that are associated with an object.



For a [ComboEx](../a-z/comboex.md) or [TreeView](../a-z/treeview.md) object, the ImageListObj property specifies the name of, or ref to, a single [ImageList](../a-z/imagelist.md) object that contains a set of images to be displayed alongside its Items. The image(s) displayed by a particular item in its normal (unselected) and selected states are specified by the corresponding element of the [ImageIndex](../a-z/imageindex.md) and [SelImageIndex](../a-z/selimageindex.md) properties respectively.


For [CoolBar](../a-z/coolbar.md), [Menu](../a-z/menu.md), and [TabControl](../a-z/tabcontrol.md) objects, the ImageListObj property specifies the name of, or ref to, a single [ImageList](../a-z/imagelist.md) object that contains a set of images for its [CoolBand](../a-z/coolband.md), [MenuItem](../a-z/menuitem.md), and [TabButton](../a-z/tabbutton.md) children respectively.


For a [ToolControl](../a-z/toolcontrol.md), ImageListObj may specify up to three [ImageList](../a-z/imagelist.md) objects that correspond to the three different states, normal, highlighted (hot) and inactive, of its [ToolButton](../a-z/toolbutton.md) children.


In all these cases, individual images are mapped to the child objects by their [ImageIndex](../a-z/imageindex.md) property.


For a [ListView](../a-z/listview.md) either one or two [ImageList](../a-z/imagelist.md) objects may be specified. The first [ImageList](../a-z/imagelist.md) contains the *large icon* set of images. the second contains the *small icon* set. The set that is used is determined by the value of the [View](../a-z/view.md) property. The mapping between the set of images in the [ImageList](../a-z/imagelist.md) and items in the object is determined by the [ImageIndex](../a-z/imageindex.md) property.


