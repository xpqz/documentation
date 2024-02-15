




<h1 class="heading"><span class="name">Animation</span></h1>

| [Parents](../ParentLists/Animation.htm) | [Children](../ChildLists/Animation.htm) | [Properties](../PropLists/Animation.htm) | [Methods](../MethodLists/Animation.htm) | [Events](../EventLists/Animation.htm) |
| --- | --- | --- | --- | ---  |


| Purpose: | The Animation object displays simple animations from basic .AVI files or resources. |
| --- | ---  |


**Description**


The Animation object displays simple animations from basic .AVI files or resources.



The Animation object can only play AVI files or resources that have no sound and can only display uncompressed AVI files or .AVI files that have been compressed using Run-Length Encoding (RLE).


For more sophisticated animations, you may use the Windows Media Player (OCX).


To display an AVI file, you must first use the [AnimOpen](./animopen.md) method to open it. If the [AutoPlay](./autoplay.md) property is set to 1, the animation will play immediately. Otherwise, only the first frame will be displayed.


The [Align](./align.md) property may be `'None'` or `'Centre'` (`'Center'`). If [Align](./align.md) is `'None'`, the Animation window is automatically resized to fit the AVI being played. If [Align](./align.md) is `'Centre'`, the AVI is centred in the Animation window. If the window is too small, the AVI is clipped.


The [AnimPlay](./animplay.md) method may be used to play the animation and allows you to specify the start, number of frames, and repeat count.


The [AnimStop](./animstop.md) method causes the animation to stop.


The [AnimClose](./animclose.md) method closes the current AVI file and resets the contents of the object's window to its background colour.


The [AnimStarted](./animstarted.md) and [AnimStopped](./animstopped.md) events are reported when the animation starts and stops respectively.


