




<h1 class="heading"><span class="name">CoolBand</span></h1>
| Parents | Children | Properties | Methods | Events |
| --- | --- | --- | --- | ---  |

| Purpose: | The CoolBand object represents an area in a CoolBar that contains a         child window. |
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


The CoolBand object is a container object that represents a band in a CoolBar.



A CoolBand can have any combination of a gripper bar, a bitmap, a text label,
and a single child object.


A CoolBand may not contain more than one child object, but that child object
may itself be a container such as a ToolControl or a SubForm.


The [Caption](./caption.md) property specifies a text
string to be displayed to the left of the CoolBand. The colour of the text is
specified by the [FCol](./fcol.md) property.


The [ImageIndex](./imageindex.md) property specifies an
optional picture which is to be displayed alongside the [Caption](./caption.md).
If specified, [ImageIndex](./imageindex.md) is an index
into an [ImageList](imagelist.md) whose name is referenced
via the [ImageListObj](./imagelistobj.md) property of the
parent CoolBar.


The background in a CoolBand may be specified using its [BCol](./bcol.md) or [Picture](./picture.md) properties. Although typically,
the visible background area is small, it is visible through a [transparent](./transparent.md) ToolControl.


The [ChildEdge](./childedge.md) property specifies
whether or not the CoolBand leaves space above and below its child window.


The [GripperMode](./grippermode.md) property specifies
whether or not the CoolBand has a gripper bar which is used to reposition and
resize the CoolBand within its parent CoolBar.
[GripperMode](./grippermode.md) may be '`Always'`(the default), `'Never'` or `'Auto'`.


The position of a Cool Band within a CoolBar is determined by its [Index](./index.md) and [NewLine](./newline.md) properties, and by the position and size of preceding CoolBand objects in the
same CoolBar. For a CoolBand, [Posn](./posn.md) is a read-only property that reports its position but [Posn](./posn.md) may not be used to set it.


The [Index](./index.md) property specifies the position
of a CoolBand within its parent CoolBar,
relative to other CoolBands and is `⎕IO` dependent. Initially, the value of [Index](./index.md) is
determined by the order in which the CoolBands are created. You may re-order the
CoolBands within a CoolBar, under program
control, by changing [Index](./index.md) with `⎕WS`.


The [NewLine](./newline.md) property specifies whether
or not the CoolBand occupies the same row as an existing CoolBand, or is
displayed on a new line within its CoolBar parent. The value of [NewLine](./newline.md) in the first
CoolBand in a CoolBar is always 1, even if
you specify it to be 0. You may move a CoolBand to the previous or next row by
changing its [NewLine](./newline.md) property (using `⎕WS`) from 1 to 0, or from 0 to 1 respectively.


The 2nd element of the [Size](./size.md) property determines the width of the CoolBand; the value of the 1st element is read-only.


[Size](./size.md) may only be specified by `⎕WC`.
However, when you create a CoolBand, it will automatically occupy all the
available space in the current row, to the right of any preceding CoolBands.
Only when you create *another* CoolBand in the *same* row, will the [Size](./size.md) of the first CoolBand be honoured. The rightmost CoolBand will always extend to
the right edge of the CoolBar, whatever its [Size](./size.md).


If you create two or more CoolBands in the same row and you do not specify [Size](./size.md),
the first CoolBand will be maximised, and the others minimised.


When the user drags a CoolBand to a different row its [Index](./index.md) and [NewLine](./newline.md) properties may change, as may
the [Index](./index.md) and [NewLine](./newline.md) properties of any another CoolBand that is affected by the operation.


If you wish to remember the user's chosen layout when your application
terminates, you must store the values of [Index](./index.md), [Size](./size.md) and [NewLine](./newline.md) for each of the CoolBands. When your application is next started, you must
re-create the CoolBands with the same values of these properties.


