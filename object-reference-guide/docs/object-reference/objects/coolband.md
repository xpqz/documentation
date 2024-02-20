




<h1 class="heading"><span class="name">CoolBand</span></h1>

[Parents](../ParentLists/CoolBand.htm) [Children](../ChildLists/CoolBand.htm) [Properties](../PropLists/CoolBand.htm) [Methods](../MethodLists/CoolBand.htm) [Events](../EventLists/CoolBand.htm)


Purpose: The CoolBand object represents an area in a CoolBar that contains a         child window.


**Description**


The CoolBand object is a container object that represents a band in a [CoolBar](../a-z/coolbar.md).



A CoolBand can have any combination of a gripper bar, a bitmap, a text label,
and a single child object.


A CoolBand may not contain more than one child object, but that child object
may itself be a container such as a [ToolControl](../a-z/toolcontrol.md) or a [SubForm](../a-z/subform.md).


The [Caption](../a-z/caption.md) property specifies a text
string to be displayed to the left of the CoolBand. The colour of the text is
specified by the [FCol](../a-z/fcol.md) property.


The [ImageIndex](../a-z/imageindex.md) property specifies an
optional picture which is to be displayed alongside the [Caption](../a-z/caption.md).
If specified, [ImageIndex](../a-z/imageindex.md) is an index
into an [ImageList](../a-z/imagelist.md) whose name is referenced
via the [ImageListObj](../a-z/imagelistobj.md) property of the
parent [CoolBar](../a-z/coolbar.md).


The background in a CoolBand may be specified using its [BCol](../a-z/bcol.md) or [Picture](../a-z/picture.md) properties. Although typically,
the visible background area is small, it is visible through a [transparent](../a-z/transparent.md) [ToolControl](../a-z/toolcontrol.md).


The [ChildEdge](../a-z/childedge.md) property specifies
whether or not the CoolBand leaves space above and below its child window.


The [GripperMode](../a-z/grippermode.md) property specifies
whether or not the CoolBand has a gripper bar which is used to reposition and
resize the CoolBand within its parent [CoolBar](../a-z/coolbar.md).
[GripperMode](../a-z/grippermode.md) may be '`Always'`(the default), `'Never'` or `'Auto'`.


The position of a Cool Band within a [CoolBar](../a-z/coolbar.md) is determined by its [Index](../a-z/index.md) and [NewLine](../a-z/newline.md) properties, and by the position and size of preceding CoolBand objects in the
same [CoolBar](../a-z/coolbar.md). For a CoolBand, [Posn](../a-z/posn.md) is a read-only property that reports its position but [Posn](../a-z/posn.md) may not be used to set it.


The [Index](../a-z/index.md) property specifies the position
of a CoolBand within its parent [CoolBar](../a-z/coolbar.md),
relative to other CoolBands and is `⎕IO` dependent. Initially, the value of [Index](../a-z/index.md) is
determined by the order in which the CoolBands are created. You may re-order the
CoolBands within a [CoolBar](../a-z/coolbar.md), under program
control, by changing [Index](../a-z/index.md) with `⎕WS`.


The [NewLine](../a-z/newline.md) property specifies whether
or not the CoolBand occupies the same row as an existing CoolBand, or is
displayed on a new line within its [CoolBar](../a-z/coolbar.md) parent. The value of [NewLine](../a-z/newline.md) in the first
CoolBand in a [CoolBar](../a-z/coolbar.md) is always 1, even if
you specify it to be 0. You may move a CoolBand to the previous or next row by
changing its [NewLine](../a-z/newline.md) property (using `⎕WS`) from 1 to 0, or from 0 to 1 respectively.


The 2<sup>nd</sup> element of the [Size](../a-z/size.md) property determines the width of the CoolBand; the value of the 1<sup>st</sup> element is read-only.


[Size](../a-z/size.md) may **only** be specified by `⎕WC`.
However, when you create a CoolBand, it will automatically occupy all the
available space in the current row, to the right of any preceding CoolBands.
Only when you create *another* CoolBand in the *same* row, will the [Size](../a-z/size.md) of the first CoolBand be honoured. The rightmost CoolBand will always extend to
the right edge of the CoolBar, whatever its [Size](../a-z/size.md).


If you create two or more CoolBands in the same row and you do not specify [Size](../a-z/size.md),
the first CoolBand will be maximised, and the others minimised.


When the user drags a CoolBand to a different row its [Index](../a-z/index.md) and [NewLine](../a-z/newline.md) properties may change, as may
the [Index](../a-z/index.md) and [NewLine](../a-z/newline.md) properties of any another CoolBand that is affected by the operation.


If you wish to remember the user's chosen layout when your application
terminates, you must store the values of [Index](../a-z/index.md), [Size](../a-z/size.md) and [NewLine](../a-z/newline.md) for each of the CoolBands. When your application is next started, you must
re-create the CoolBands with the same values of these properties.


