




<h1 class="heading"><span class="name">KeepBits</span></h1>

| Applies To: | [Bitmap](../a-z/bitmap.md) | [Cursor](../a-z/cursor.md) | [Icon](../a-z/icon.md) |
| --- | --- | --- | ---  |


**Description**


This property is be used to control the way that [Bitmap](../a-z/bitmap.md), [Cursor](../a-z/cursor.md) and [Icon](../a-z/icon.md) objects are stored in the workspace.


When you create a [Bitmap](../a-z/bitmap.md), [Icon](../a-z/icon.md) or [Cursor](../a-z/cursor.md) using `⎕WC`, APL asks Windows to allocate a corresponding bitmap, icon or cursor *resource*. This resource is allocated in Windows memory. If APL were to hold the values of the *image properties* ([CBits](../a-z/cbits.md), [Bits](../a-z/bits.md) and [CMap](../a-z/cmap.md) for a [Bitmap](../a-z/bitmap.md); [Bits](../a-z/bits.md), [CMap](../a-z/cmap.md) and [Mask](../a-z/mask.md) for [Cursor](../a-z/cursor.md) and [Icon](../a-z/icon.md) objects) internally in the workspace, this data would be duplicated. For large bitmaps this would have a serious impact on memory utilisation and may affect performance. The KeepBits property is provided to allow you to control whether or not APL retains the values of the *image properties* in the workspace, so that you can choose a strategy to suit your configuration and requirements. KeepBits may take the value 0 or 1.


If KeepBits is 0 the values of the *image properties* are **not** stored internally in your workspace. If you save a workspace containing a [Bitmap](../a-z/bitmap.md), [Cursor](../a-z/cursor.md) or [Icon](../a-z/icon.md) object, the corresponding Windows resource is automatically re-allocated when the workspace is loaded by referring to the associated file. This is the file whose full pathname is defined by the value of the object's [File](../a-z/file.md) property. It follows that if you adopt this strategy, you must ensure that the [File](../a-z/file.md) property is set correctly. If APL cannot find the file when the workspace is `)LOAD`ed, it cannot re-create the object, and you will get a `VALUE ERROR` when you subsequently refer to it. A further consideration is the effect on `⎕WG`. If KeepBits is 0, and you execute `⎕WG 'CBits'` or `'Bits'` or `'CMap'` or `'Mask'`, APL obtains these values by requesting the data from Windows.


If KeepBits is set to 1, the contents of the *image properties* are stored in the workspace, thus duplicating the information which is held by Windows itself. If you save a workspace containing a [Bitmap](../a-z/bitmap.md), [Cursor](../a-z/cursor.md) or [Icon](../a-z/icon.md) the corresponding Windows resource is automatically re-allocated from the *image properties* when the workspace is loaded. The value of the [File](../a-z/file.md) property is ignored. When you execute `⎕WG 'CBits'` or `'Bits'` or `'CMap'` or `'Mask'`, APL generates the result directly from the stored values held (internally) in the workspace.



